
## Enable Template Hints from URL

`vendor/magento/module-developer/Model/TemplateEngine/Plugin/DebugHints.php`
write this code inside afterCreate function : (at the start, above the storecode line)
```sh
if(isset($_GET['hints']) && $_GET['hints'] == 'on'){
    return $this->debugHintsFactory->create([
        'subject' => $invocationResult,
        'showBlockHints' => 1,
    ]);
}
```
Now, you can open any Magento page and append ?hints=on to the URL. No need to run any commands.

## Enable AutoAdmin Login

`vendor/magento/module-backend/Model/Auth.php`

## Stop checkout success page redirection after refresh page

`vendor/magento/module-checkout/Controller/Onepage/Success.php`
Comment Out Line No : 26 (in Magento 2.4)
```sh
//$session->clearQuote();
```

## Log sql queries to File

`vendor/magento/framework/DB/Statement/Pdo/Mysql.php`
inside _execute function before "if ($specialExecute) {"
```sh
file_put_contents(BP . '/var/log/ShreyasParams.log', print_r($this->_stmt->queryString, true) . PHP_EOL . (!empty($params) ? json_encode($params, true) . PHP_EOL : ''), FILE_APPEND);
```


## Disable twofactorauth

`vendor\magento\module-two-factor-auth\Model\TfaSession.php`
```sh
/**
 * @inheritDoc
 */
public function isGranted(): bool
{
    return true;//(bool) $this->storage->getData(TfaSessionInterface::KEY_PASSED);
}
```
