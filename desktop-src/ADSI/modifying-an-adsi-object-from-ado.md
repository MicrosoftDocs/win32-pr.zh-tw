---
title: 從 ADO 修改 ADSI 物件
description: 適用于 Windows 2000 和 DS 用戶端的 ADSI 包含唯讀的 OLE DB 提供者。 這表示您目前無法在 SQL 方言中發出 UPDATE 語句。
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- 從 ADO ADSI 修改 ADSI 物件
- ActiveX 資料物件 ADSI，從 ADO 修改 ADSI 物件
- ADSI ADSI，範例程式碼 C/c + +，修改 ADSI 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7291088915a537231077e1d75161b57684caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671139"
---
# <a name="modifying-an-adsi-object-from-ado"></a><span data-ttu-id="4a449-107">從 ADO 修改 ADSI 物件</span><span class="sxs-lookup"><span data-stu-id="4a449-107">Modifying an ADSI Object from ADO</span></span>

<span data-ttu-id="4a449-108">適用于 Windows 2000 和 DS 用戶端的 ADSI 包含唯讀的 OLE DB 提供者。</span><span class="sxs-lookup"><span data-stu-id="4a449-108">ADSI for Windows 2000 and DS Client includes a read-only OLE DB provider.</span></span> <span data-ttu-id="4a449-109">這表示您目前無法在 SQL 方言中發出 UPDATE 語句。</span><span class="sxs-lookup"><span data-stu-id="4a449-109">This means that you cannot, at present, issue the UPDATE statement in the SQL dialect.</span></span>

<span data-ttu-id="4a449-110">**修改從 ADO 查詢傳回的物件**</span><span class="sxs-lookup"><span data-stu-id="4a449-110">**To modify an object returned from an ADO query**</span></span>

1.  <span data-ttu-id="4a449-111">指定屬性名稱時，請要求 **ADsPath** ，如同「選取 ADsPath，...」。</span><span class="sxs-lookup"><span data-stu-id="4a449-111">Request the **ADsPath** when specifying an attribute name, as in "SELECT ADsPath, ..."</span></span>
2.  <span data-ttu-id="4a449-112">執行查詢並取得 **ADsPath** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4a449-112">Execute the query and get the **ADsPath** attribute.</span></span>
3.  <span data-ttu-id="4a449-113">使用 **ADsPath** 系結至記錄集，並修改屬性。</span><span class="sxs-lookup"><span data-stu-id="4a449-113">Bind to the record set using **ADsPath**, and modify the attributes.</span></span>

<span data-ttu-id="4a449-114">下列程式碼範例示範如何在執行上述範例中所述的步驟之後修改 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="4a449-114">The following code example shows how to modify an ADSI object after performing the steps outlined in the preceding example.</span></span>


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




