| PHP Native / Superglobal | Magento / Adobe Commerce Alternative |
| ------------------------ | ------------------------------------ |
| $_GET | \Magento\Framework\App\RequestInterface::getParam() |
| $_POST | \Magento\Framework\App\RequestInterface::getPostValue() |
| $_REQUEST | ❌ Avoid (use RequestInterface explicitly) |
| $_FILES | \Magento\Framework\App\RequestInterface::getFiles() |
| $_SERVER | \Magento\Framework\HTTP\PhpEnvironment\Request |
| $_COOKIE | \Magento\Framework\Stdlib\CookieManagerInterface |
| $_SESSION | \Magento\Framework\Session\SessionManagerInterface |
| $_ENV | \Magento\Framework\App\Config\ScopeConfigInterface |
| strlen() | \Magento\Framework\Stdlib\StringUtils::strlen() |
| substr() | \Magento\Framework\Stdlib\StringUtils::substr() |
| strpos() | \Magento\Framework\Stdlib\StringUtils::strpos() |
| strtolower() | \Magento\Framework\Stdlib\StringUtils::strtolower() |
| strtoupper() | \Magento\Framework\Stdlib\StringUtils::strtoupper() |
| trim() | \Magento\Framework\Stdlib\StringUtils::trim() |
| base64_encode() | \Magento\Framework\Encryption\EncryptorInterface::encrypt() |
| base64_decode() | \Magento\Framework\Encryption\EncryptorInterface::decrypt() |
| json_encode() | \Magento\Framework\Serialize\Serializer\Json::serialize() |
| json_decode() | \Magento\Framework\Serialize\Serializer\Json::unserialize() |
| serialize() | \Magento\Framework\Serialize\SerializerInterface::serialize() |
| unserialize() | \Magento\Framework\Serialize\SerializerInterface::unserialize() |
| file_get_contents() | \Magento\Framework\Filesystem\Driver\File::fileGetContents() |
| file_put_contents() | \Magento\Framework\Filesystem\Driver\File::filePutContents() |
| file_exists() | \Magento\Framework\Filesystem\Driver\File::isExists() |
| unlink() | \Magento\Framework\Filesystem\Driver\File::deleteFile() |
| mkdir() | \Magento\Framework\Filesystem\Directory\WriteInterface::create() |
| copy() | \Magento\Framework\Filesystem\Driver\File::copy() |
| rename() | \Magento\Framework\Filesystem\Driver\File::rename() |
| glob() | \Magento\Framework\Filesystem\Driver\File::readDirectory() |
| curl_* | \Magento\Framework\HTTP\Client\Curl |
| file_get_contents(URL) | \Magento\Framework\HTTP\Client\Curl |
| header() | \Magento\Framework\App\Response\Http |
| date() | \Magento\Framework\Stdlib\DateTime\DateTime |
| time() | \Magento\Framework\Stdlib\DateTime\DateTime::gmtTimestamp() |
| strtotime() | \Magento\Framework\Stdlib\DateTime\DateTime |
| rand() | \Magento\Framework\Math\Random |
| mt_rand() | \Magento\Framework\Math\Random |
| md5() | ❌ Avoid (use EncryptorInterface) |
| sha1() | ❌ Avoid (use EncryptorInterface) |
| password_hash() | \Magento\Framework\Encryption\EncryptorInterface |
| hash() | \Magento\Framework\Encryption\EncryptorInterface |
| echo | Block / Template rendering |
| print_r() | \Psr\Log\LoggerInterface |
| var_dump() | \Psr\Log\LoggerInterface |
| die() | Throw \Magento\Framework\Exception\LocalizedException |
| exit() | Throw Exception |
| getenv() | \Magento\Framework\App\Config\ScopeConfigInterface |
| ini_get() | ❌ Avoid |
| ini_set() | ❌ Avoid |
| phpinfo() | ❌ Never allowed |
| mail() | \Magento\Framework\Mail\Template\TransportBuilder |
| setcookie() | \Magento\Framework\Stdlib\CookieManagerInterface |
| error_log() | \Psr\Log\LoggerInterface |
| sleep() | ❌ Avoid |
| usleep() | ❌ Avoid |
