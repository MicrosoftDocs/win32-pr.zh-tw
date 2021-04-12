---
title: ADSI) 驗證 (
description: 在 ADSI 中，使用者名稱和密碼所組成的認證是用來提供或限制存取目錄服務中的物件。
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- 驗證 ADSI
- ADSI、使用、驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad32b2f32f115b20c99e47578ad76b73ad72a123
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104462724"
---
# <a name="authentication-adsi"></a><span data-ttu-id="0d454-105">ADSI) 驗證 (</span><span class="sxs-lookup"><span data-stu-id="0d454-105">Authentication (ADSI)</span></span>

<span data-ttu-id="0d454-106">在 ADSI 中，使用者名稱和密碼所組成的認證是用來提供或限制存取目錄服務中的物件。</span><span class="sxs-lookup"><span data-stu-id="0d454-106">In ADSI, credentials that consist of a user name and password are used to provide or restrict access to objects in the directory service.</span></span> <span data-ttu-id="0d454-107">[**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)函式會使用呼叫執行緒的認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="0d454-107">The [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function uses the credentials of the calling thread for authentication.</span></span> <span data-ttu-id="0d454-108">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)函式和 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)方法可以用來指定除了呼叫執行緒以外的認證。</span><span class="sxs-lookup"><span data-stu-id="0d454-108">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method can be used to specify credentials other than those of the calling thread.</span></span> <span data-ttu-id="0d454-109">當物件與已驗證的使用者系結時，會允許使用者存取基礎目錄服務安全性需求所支援的物件。</span><span class="sxs-lookup"><span data-stu-id="0d454-109">When an object is bound to with an authenticated user, the user is allowed access to the object as supported by the underlying directory service security requirements.</span></span>

> [!Note]  
> <span data-ttu-id="0d454-110">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)函式和 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)方法不應用來驗證使用者認證。</span><span class="sxs-lookup"><span data-stu-id="0d454-110">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method should not be used to validate user credentials.</span></span> <span data-ttu-id="0d454-111">如需驗證使用者認證的詳細資訊，請參閱 Microsoft 知識庫文章 180548 [做法：驗證 Microsoft 作業系統上的使用者認證](https://support.microsoft.com/kb/180548)。</span><span class="sxs-lookup"><span data-stu-id="0d454-111">For more information about validating user credentials, see Microsoft Knowledge Base article 180548 [HOWTO: Validate User Credentials on Microsoft Operating Systems](https://support.microsoft.com/kb/180548).</span></span>

 

<span data-ttu-id="0d454-112">下列程式碼範例顯示如何使用 [**objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 方法來驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="0d454-112">The following code example shows how to use the [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method to authenticate a user.</span></span>


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




