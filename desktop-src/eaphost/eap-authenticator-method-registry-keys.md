---
title: EAP Authenticator 方法登錄值
description: 瞭解 EAP Authenticator 方法登錄值。 EAP 驗證器方法需要這些特定的登錄值。
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1db88a910a40519533ffddae40c1e1cc04d36b62f3d3ad6543ddd4a2999373e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984308"
---
# <a name="eap-authenticator-method-registry-values"></a>EAP Authenticator 方法登錄值

EAP 驗證器方法需要特定的登錄值。

## <a name="eap-authenticator-method-dll-paths"></a>EAP Authenticator 方法 DLL 路徑

下列路徑指定一般 EAP 驗證器方法 Dll 的登錄位置。

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ *&lt; 作者 &gt;* \\ * &lt; EapTypeId&gt;***

例如，EAP 驗證器方法安裝註冊路徑 **指定了 "** 311" (表示 "Microsoft" 是作者) ，而 **EapTypeId** "40"，如下所示。

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ 311 \\ 40**

下列路徑指定擴充 EAP 驗證器方法 Dll 的登錄位置。

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ *&lt; 作者 &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; VendorType&gt;***

例如，EAP 驗證器方法安裝註冊路徑 **指定了 "** 311" (表示 "Microsoft" 是作者) 、"311" 的 **VendorId** 和 "40" 的 **EapTypeId** ，如下所示。

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> 如需 EAP 方法類型配置的詳細資訊，請參閱 [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)的6.2 節。

 

## <a name="registry-values"></a>登錄值

以下是必要的驗證器方法登錄值。

-   [AuthenticatorDllPath](#authenticatordllpath)
-   [AuthenticatorFriendlyName](#authenticatorfriendlyname)

除了上述的登錄值，建議使用下列驗證器方法登錄值。

-   [屬性](#properties)

其餘的驗證器方法登錄值是選擇性的。

-   [ConfigCLSID](#configclsid)
-   [StandaloneSupported](#standalonesupported)

## <a name="authenticatordllpath"></a>AuthenticatorDllPath



| 常數值 | AuthenticatorDllPath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| 類型           | REG \_ EXPAND \_ SZ                                                                                               |
| 描述    | EAP 驗證器方法 DLL 的路徑。 例如， \\ \\ &lt; \_ \_ DLL &gt;.dll 的% SystemRoot% system32 名稱。 |



 

## <a name="authenticatorfriendlyname"></a>AuthenticatorFriendlyName



| 常數值 | AuthenticatorFriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| 類型           | REG \_ SZ                                                                            |
| 描述    | 包含易記 (顯示 EAP 驗證器方法) 名稱的字串。 |



 

## <a name="configclsid"></a>ConfigCLSID



| 常數值 | ConfigCLSID                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG \_ SZ                                                                                                                               |
| 描述    | 字串，其中包含此驗證器方法的設定類別 GUID，格式為 {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} |



 

## <a name="properties"></a>屬性



| 常數值 | 屬性                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG \_ DWORD                                                                                                                                                  |
| 描述    | DWORD 中的位會設定為指出屬性的支援。 如需支援值的清單，請參閱 [**EAP 方法屬性**](eap-method-properties.md)。 |



 

## <a name="standalonesupported"></a>StandaloneSupported



| 常數值 | StandaloneSupported                                             |
|----------------|-----------------------------------------------------------------|
| 類型           | REG \_ DWORD                                                      |
| 描述    | 如果這是獨立的驗證器方法，則為 0;如果不是，則為1。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAP 對等方法登錄機碼](eap-peer-method-registry-keys.md)
</dt> <dt>

[擴充的 EAP 類型的登錄設定](registry-keys-for-eap-methods.md)
</dt> <dt>

[使用 EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




