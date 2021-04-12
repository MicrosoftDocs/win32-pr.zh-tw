---
title: EAP 對等方法登錄值
description: 瞭解 EAP 對等方法所需的特定登錄值。 查看登錄值的清單，並查看其他可用的資源。
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316492"
---
# <a name="eap-peer-method-registry-values"></a>EAP 對等方法登錄值

EAP 對等方法需要特定的登錄值。

## <a name="eap-peer-method-dll-paths"></a>EAP 對等方法 DLL 路徑

下列路徑指定一般 EAP 對等方法 Dll 的登錄位置。

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ *&lt; 作者 &gt;* \\ * &lt; EapTypeId&gt;***

例如，假設 "311" 的 **作者為 "** " 的 EAP 方法安裝註冊路徑 (表示 "Microsoft" 是作者) ，而 **EapTypeId** "40"，則會顯示如下。

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ 311 \\ 40**

下列路徑指定擴充的 EAP 方法 Dll 的登錄位置。

> [!Note]  
> Windows Vista Service Pack 1 (SP1) 或更新版本支援擴充的 EAP 方法 Dll。

 

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ *&lt; 作者 &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; EapTypeId&gt;***

例如，假設 "311" 的 **作者為 "** " 的 EAP 方法安裝註冊路徑 (表示 "Microsoft" 是作者) 、"311" 的 **VendorId** 和 "40" 的 **EapTypeId** ，如下所示。

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ 方法 \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> 如需 EAP 方法類型配置的詳細資訊，請參閱 [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)的6.2 節。

 

## <a name="registry-values"></a>登錄值

需要下列 EAPHost 對等方法登錄值。

-   [PeerDllPath](#peerdllpath)
-   [PeerFriendlyName](#peerfriendlyname)
-   [PeerInvokePasswordDialog](#peerinvokepassworddialog)
-   [PeerInvokeUsernameDialog](#peerinvokeusernamedialog)

建議使用下列 AP 對等方法登錄值。

-   [屬性](#properties)

下列 AP 對等方法登錄值是選擇性的。

-   [PeerConfigUIPath](#peerconfiguipath)
-   [PeerIdentityPath](#peeridentitypath)
-   [PeerInteractiveUIPath](#peerinteractiveuipath)
-   [PeerRequireConfigUI](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>PeerConfigUIPath



| 常數值 | PeerConfigUIPath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG \_ EXPAND \_ SZ                                                                                                                                        |
| Description    | 包含 [使用者設定] 對話方塊之 [執行] 的 DLL 路徑。 例如，% SystemRoot% \\ system32 \\ &lt; 的名稱 \_ 為 \_ .dll &gt; 。 |



 

### <a name="peerdllpath"></a>PeerDllPath



| 常數值 | PeerDllPath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| 類型           | REG \_ EXPAND \_ SZ                                                                                 |
| Description    | EAP 方法 DLL 的路徑。 例如，% SystemRoot% \\ system32 \\ &lt; 的名稱 \_ 為 \_ .dll &gt; 。 |



 

### <a name="peerfriendlyname"></a>PeerFriendlyName



| 常數值 | PeerFriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| 類型           | REG \_ SZ                                                              |
| Description    | 包含易記 (顯示 EAP 方法) 名稱的字串。 |



 

### <a name="peeridentitypath"></a>PeerIdentityPath



| 常數值 | PeerIdentityPath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG \_ EXPAND \_ SZ                                                                                                                                      |
| Description    | DLL 的路徑，其中包含使用者識別函式的執行。 例如，% SystemRoot% \\ system32 \\ &lt; 的名稱 \_ 為 \_ .dll &gt; 。 |



 

### <a name="peerinteractiveuipath"></a>PeerInteractiveUIPath



| 常數值 | PeerInteractiveUIPath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG \_ EXPAND \_ SZ                                                                                                                                                                                                            |
| Description    | DLL 的路徑，其中包含在執行 EAP 方法期間用來取得使用者資訊的互動式使用者介面。 例如，% SystemRoot% \\ system32 \\ &lt; 的名稱 \_ 為 \_ .dll &gt; 。 |



 

### <a name="peerinvokepassworddialog"></a>PeerInvokePasswordDialog



| 常數值 | PeerInvokePasswordDialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG \_ DWORD                                                                                                                                                                                                                                       |
| Description    | 1-使用一般 EAPHost 密碼和網域對話方塊取得認證。 0-使用自訂對話方塊。 如果使用一般對話方塊，則會由 [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) 方法設定認證。 |



 

### <a name="peerinvokeusernamedialog"></a>PeerInvokeUsernameDialog



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>常數值</th>
<th>PeerInvokeUsernameDialog</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>類型</td>
<td>REG_DWORD</td>
</tr>
<tr class="even">
<td>Description</td>
<td><ul>
<li>1-使用 [一般 EAPHost 使用者名稱] 對話方塊來取得認證。</li>
<li>0-使用自訂對話方塊。</li>
</ul>
如果使用 [一般] 對話方塊，則認證會由 [<strong>EapPeerSetCredentials</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials]) 方法設定。</td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a>PeerRequireConfigUI



| 常數值 | PeerRequireConfigUI                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| 類型           | REG \_ DWORD                                                                                 |
| Description    | 如果此方法的設定使用者介面對話方塊已執行，則為0。如果不是，則為1。 |



 

### <a name="properties"></a>屬性



| 常數值 | 屬性                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類型           | REG \_ DWORD                                                                                                                                                  |
| Description    | DWORD 中的位會設定為指出屬性的支援。 如需支援值的清單，請參閱 [**EAP 方法屬性**](eap-method-properties.md)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAP 驗證器方法登錄機碼](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[擴充的 EAP 類型的登錄設定](registry-keys-for-eap-methods.md)
</dt> <dt>

[使用 EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 