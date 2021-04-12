---
title: OutputType 複雜型別
description: 定義輸出資料類型，以決定如何呈現資料。
ms.assetid: a15fc5b0-d9af-4786-b322-63b5ecc326b2
keywords:
- OutputType 複雜型別 EventLog
topic_type:
- apiref
api_name:
- OutputType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3dd46b1f18b087470387481d50a462b8ed97b3e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464565"
---
# <a name="outputtype-complex-type"></a>OutputType 複雜型別

定義輸出資料類型，以決定如何呈現資料。

``` syntax
<xs:complexType name="OutputType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="default"
                type="boolean"
                use="optional"
             />
            <xs:attribute name="xmlType"
                type="QName"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱    | 類型      | Description                                                                                                                                                                                       |
|---------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 預設 | boolean   | 判斷此輸出類型是否應該當做父輸入類型的預設輸出類型使用。 設定為 **true** 以使用此輸出類型作為預設類型;否則 **為 false**。<br/> |
| xmlType | **QName** | 輸出類型的名稱。<br/>                                                                                                                                                           |



## <a name="remarks"></a>備註

以下列出您可以在資訊清單中指定的可辨識輸出類型。 輸出類型會決定服務呈現資料的方式。 輸出類型定義在包含 \\ 于 Windows SDK 的 IncludeWinmeta.xml 檔案中 \\ 。

**Windows Server 2008 和 Windows Vista：** 服務不會使用輸出類型來呈現資料。相反地，服務會使用輸入類型來決定如何呈現資料。



| 輸出類型                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xs:string                      | 文字資料。 此類型對 UnicodeString 和 AnsiString 輸入類型有效。 從隨附于 Windows Server 2016 SDK 或更新版本的 mc.exe (mc.exe 10.0.14251 版或更新版本的) 中，此類型也適用于 Int8、UInt8 和 UInt16 輸入類型，在這種情況下，資料會轉譯為單一字元。                                                                                                                                                                                                                                                                                                           |
| xs:datetime                    | XML 日期/時間。 這是所有日期的預設格式。 日期是使用內嵌在字串中的文化特性標記來格式化 (例如，由左至右或由右至左) 。 如需格式化日期和時間的相關資訊，請參閱 MSDN 上的取得日期和時間資訊。 此類型對 FILETIME 和 SYSTEMTIME 輸入類型有效。 在 **Windows 7 版 Windows SDK 隨附的 MC 編譯器版本之前：** 日期不是使用內嵌在字串中的文化特性標記來轉譯 (例如，由左至右或由右至左) 。<br/>                                                  |
| xs:byte                        | 格式化為十進位整數的帶正負號8位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| xs:unsignedByte                | 格式化為十進位整數的不帶正負號8位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| xs:short                       | 格式化為十進位整數的帶正負號16位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| xs:unsignedShort               | 格式化為十進位整數的不帶正負號16位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| xs:int                         | 格式化為十進位整數的帶正負號32位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| xs:unsignedInt                 | 格式化為十進位整數的不帶正負號32位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| xs:long                        | 格式化為十進位整數的帶正負號64位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| xs:unsignedLong                | 格式化為十進位整數的不帶正負號64位整數                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| xs:float                       | 4 位元組浮點數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| xs:double                      | 8 位元組浮點數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| xs:boolean                     | 布林值。 此類型對於布林輸入類型有效，表示對應至 Win32 BOOL 類型的32位布林值。 從隨附于 Windows Server 2016 SDK 或更新版本的 mc.exe (mc.exe 10.0.14251 版或更新版本的) 中，此類型也適用于 UInt8 輸入類型，表示對應至 c + + bool 和 Win32 布林值類型的8位布林值。                                                                                                                                                                                                                                             |
| xs:GUID                        | 以登錄字串格式（{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}）進行格式化的 GUID 值。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| xs:hexBinary                   | 一系列的十六進位數位。 格式化資料的每個位元組都會以前置零填補。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| win： HexInt8                    | 前面加上 "0x" 的十六進位數位。 格式化的值不會以前置零填補。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| win： HexInt16                   | 前面加上 "0x" 的十六進位數位。 格式化的值不會以前置零填補。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| win： HexInt32                   | 前面加上 "0x" 的十六進位數位。 格式化的值不會以前置零填補。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| win： HexInt64                   | 前面加上 "0x" 的十六進位數位。 格式化的值不會以前置零填補。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| win： PID                        | 表示處理序識別碼的帶正負號32位整數。 此值會格式化為十進位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| win： TID                        | 表示執行緒 ID 的帶正負號32位整數。 此值會格式化為十進位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| win： Port                       | 表示 IP 位址埠的帶正負號16位整數。 將值傳遞至 [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) 函式，並將結果格式化為十進位整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| win： IPv4                       | IPv4 IP 位址。 此類型對 UInt32 輸入類型有效。 值必須是網路位元組順序;UInt32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。 位址會以點標記法格式化。 <br/> 若要將包含 IPv4 位址的不帶正負號的整數轉換成字串，請呼叫 [**RtlIpv4AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa) 或 [**inet \_ ntoa**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa) 函數。<br/>                                                                        |
| win： IPv6                       | IPv6 IP 位址。 此類型對 win： Binary 輸入類型有效。 位址會格式化為字串。 若要格式化位址，請呼叫 [**RtlIpv6AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa) 函數。                                                                                                                                                                                                                                                                                                                                                                                                                                |
| win： SocketAddress              | 解釋為 **SOCKADDR \_ 儲存** 結構的通訊端位址。 位址系列會決定位址的格式化方式。 若為 AF \_ INET 和 af \_ INET6 系列，位址會格式化為 \_ 所有其他系列 <IP 位址>： <Port> ;，則會將位址格式化為十六進位轉儲。<br/> 若為 AF \_ INET 和 af \_ INET6，事件資料會是128位的二進位值。 若為 AF \_ 連結，事件資料會是112位的二進位值。<br/> **Windows Server 2008 和 Windows Vista：**\_不支援 AF 連結位址系列。<br/>                                                                            |
| win： CIMDateTime                | 代表 CIM 日期/時間。 指定時間戳記或間隔。 如果指定時間戳記，則會保留時區位移。 不支援。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| win： DateTimeCultureInsensitive | XML 日期/時間。 此類型對 FILETIME 和 SYSTEMTIME 輸入類型有效。 日期不是使用內嵌在字串中的文化特性標記來轉譯 (例如，由左至右或由右至左) 。 如需格式化日期和時間的相關資訊，請參閱 MSDN 上的取得日期和時間資訊。**在 MC 版本1.12.7051 和 Windows 7 之前：** 無法使用<br/>                                                                                                                                                                                                                                                           |
| win： Xml                        | XML 檔或檔片段。 此類型對 UnicodeString 和 AnsiString 輸入類型有效。 當您在執行 Windows Server 2016 或更新版本的系統上解碼時，搭配 AnsiString 輸入類型使用時，除非 XML 檔以指定替代編碼的處理指示開頭，否則會將字串視為 UTF-8。                                                                                                                                                                                                                                                                                          |
| win： ETWTIME                    | 時間戳記，以100毫微秒單位為單位，這是從追蹤開始到寫入事件時的相對時間。 時間戳記會轉譯為十進位整數。 此類型對 UInt32 或 UInt64 輸入類型有效。                                                                                                                                                                                                                                                                                                                                                                                                           |
| win： ErrorCode                  | 錯誤碼。 此類型對 UInt32 輸入類型有效。 程式碼會轉譯為十六進位數位，前面會加上 "0x"。 請勿使用，而是改用更明確的錯誤碼類型，例如 Win32Error 或 HResult。                                                                                                                                                                                                                                                                                                                                                                                                                  |
| win： Win32Error                 | Win32 錯誤碼。 此類型對 UInt32 輸入類型有效。 服務會抓取並轉譯與 Win32 錯誤碼相關聯的訊息字串（如果有的話）;否則，服務會轉譯格式為「未知的 Win32 錯誤碼：0x」的字串，並將 Win32 錯誤碼附加為十六進位數位。                                                                                                                                                                                                                                                                                                                         |
| win： NTSTATUS                   | NTSTATUS 錯誤碼。 此類型對 UInt32 輸入類型有效。 服務會抓取並轉譯與 NT 狀態碼相關聯的訊息字串（如果有的話）;否則，服務會轉譯格式為「未知的 NTSTATUS 錯誤碼：0x」的字串，並將 NT 狀態碼附加為十六進位數位。**在 MC 版本1.12.7051 和 Windows 7 之前：** 無法使用<br/>                                                                                                                                                                                                                                             |
| win： HResult                    | HRESULT 錯誤碼。 此類型對 Int32 輸入類型有效。 服務會抓取並轉譯與 HRESULT 錯誤碼相關聯的訊息字串（如果有的話）;否則，服務會轉譯格式為「未知的 HResult 錯誤碼：0x」的字串，並以十六進位數位的形式附加 HRESULT 錯誤碼。**在 MC 版本1.12.7051 和 Windows 7 之前：** 無法使用<br/>                                                                                                                                                                                                                                        |
| win： Json                       | JSON 字串。 此類型對 UnicodeString 和 AnsiString 輸入類型有效。 搭配 AnsiString 輸入類型使用時，字串會被視為 UTF-8。                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| win： Utf8                       | UTF-8 字串。 此類型對 AnsiString 輸入類型有效。 使用這個輸出型別時，字串會被視為 UTF-8。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| win： Pkcs7WithTypeInfo          | \#具有選擇性類型資訊的 PKCS 7 訊息。 此類型對二進位輸入類型有效。 資料包含 PKCS \# 7 訊息 (例如加密及/或已簽署的資料) ，選擇性地接著描述內部內容類型的 TraceLogging 類型資訊。 例如，可能會附加 byte 0x01 (TlgInUNICODESTRING = 0x01) ，表示內部內容會被解釋為輸入類型 UnicodeString;可能會附加 bytes 0x82 0x22 (TlgInANSISTRING + TlgInChain = 0x82，TlgOutJSON = 0x22) ，表示內部內容會被解釋為輸入類型 AnsiString、輸出類型 Json。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

