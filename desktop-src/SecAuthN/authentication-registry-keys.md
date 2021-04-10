---
description: 當它安裝網路提供者時，您的應用程式應該建立登錄機碼，以及本主題中所述的值。
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: 驗證登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944464"
---
# <a name="authentication-registry-keys"></a>驗證登錄機碼

當它安裝網路提供者時，您的應用程式應該建立登錄機碼，以及本主題中所述的值。 這些索引鍵和值提供有關系統上所安裝網路提供者的 MPR 資訊。 MPR 會在啟動時檢查這些金鑰，並載入其找到的網路提供者 Dll。

在您建立一組金鑰來保存網路提供者的相關資訊之前，您應該將網路提供者的名稱新增至 **訂單** 金鑰。 此金鑰是下列機碼的子機碼：

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

**Order** 索引鍵包含單一值 **ProviderOrder**，它會列出已安裝的提供者，並指定在作業期間，在提供者之間迴圈處理的順序，直到找到接受的提供者為止。

**ProviderOrder** 值包含以逗號分隔的索引鍵名稱清單。 **ProviderOrder** 中的每個索引鍵名稱都會識別網路提供者。 當 MPR 迴圈處理提供者時，它會依其出現在這份清單中的順序來呼叫它們。

您也應該在 **ProviderOrder** 中設定提供者名稱，作為包含該提供者相關資訊的登錄機碼名稱。 提供者特定的登錄機碼會建立為下列機碼的子機碼：

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

換句話說， **ProviderOrder** 中指定的提供者名稱是網路提供者特定金鑰登錄的路徑，相對於下列路徑：

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

當您的網路提供者服務安裝完成時，安裝應用程式應新增金鑰，如下所示：

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

其中 *ProviderName* 是在 **order** 索引鍵的 **ProviderOrder** 值中所指定的網路提供者名稱。 *ProviderName* 索引鍵下的 **群組** 值應該設定為 "NetworkProvider"。 這會將服務識別為在網路提供者群組中。

您也必須建立 *ProviderName*、 **networkprovider** 的子機碼。 此索引鍵包含描述網路提供者的下列值。



| 值                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **名稱**<br/>         | 包含提供者的名稱。 在 [流覽] 對話方塊中，使用者會看到此名稱做為網路的名稱，且應符合 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea)結構中傳回的 **lpProvider** 欄位。 這個名稱應該是產品名稱的一些變化，最好也要有公司的某些指示，讓它成為清楚且獨一無二的。 例如，"MS-LanMan" 是不錯的名稱，而 "Net" 則是不佳的選擇。<br/> |
| **ProviderPath**<br/> | 包含可執行網路提供者之 DLL 的完整路徑。 MPR 會在此路徑上呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 。<br/>                                                                                                                                                                                                                                                                                                                                |



 

下列值僅供支援認證管理函式（ [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) 和 [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)）的網路提供者使用。



| 值                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **類別**<br/>               | **DWORD** ，識別此提供者支援之提供者功能的類別或類型。 值可能會在適當時由 **OR** 運算子聯結。 此值的有效值為 WN \_ NETWORK \_ CLASS、WN \_ CREDENTIAL \_ class、WN \_ PRIMARY \_ AUTHENT \_ class 和 WN \_ SERVICE \_ 類別。<br/> 雖然提供者可能支援主要驗證器功能，但另一種方法則是用來判斷哪個驗證器是主要的。<br/> **WINDOWS XP/2000：** 不支援切換主要驗證器，所以會忽略此值。 <br/> |
| **AuthentProviderPath**<br/> | 這是匯出認證管理功能之 DLL 的完整檔案名。 此值很有用 (但只有在將提供者識別為認證 \_ 類別或主要 \_ AUTHENT \_ 類別提供者時，才需要) 。 如果這個類別的提供者沒有這個值，則應該從 ProviderPath 值所識別的 DLL 匯出認證管理函式。 只有在需要將網路功能和認證管理員函式封裝在不同的 Dll 時，才會使用此值。<br/>  |



 

除了用來註冊網路提供者和認證管理員的值之外，您還可以將值新增至登錄，以註冊 DLL 以接收連接通知。 若要這樣做，請在下列機碼底下建立 REG \_ EXPAND \_ SZ 值：

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

此值應指定可執行 [連接通知 API](connection-notification-api.md)之 DLL 的路徑。 此值的名稱可以是任何您想要的名稱，前提是它不會與預先存在的值名稱衝突。

## <a name="example"></a>範例

下列範例顯示安裝了兩個網路提供者的系統登錄機碼： LanmanWorkStation 和 AnotherNetSvc。 AnotherNetSvc 也是認證管理員。 在此範例中，索引鍵名稱為粗體，而值名稱為斜體。

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **NetworkProvider** \\ **順序**

*ProviderOrder* = "LanmanWorkStation，AnotherNetSvc"

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **NetworkProvider** \\ **Notifyees**

*MyNotifyApp* = "c： \\ connect \\connect.dll"

**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**\\

*Group* = "NetworkProvider"

**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Class* = 0X00000001 (WN \_ NETWORK \_ 類別) 

**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**\\

*Group* = "NetworkProvider"

**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**

*Name* = "其他網路"*ProviderPath* = "c： \\ 其他 \\anet.dll"

*Class* = 0X00000003 (WN \_ NETWORK \_ Class \| WN \_ CREDENTIAL \_ class) 

*AuthentProviderPath* = "c： \\ 其他 \\anetCM.dll"

 

