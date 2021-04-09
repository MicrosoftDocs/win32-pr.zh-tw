---
title: 使用 ActiveX 資料物件系結至 ADSI 提供者
description: 因為 ADSI 也是 OLE DB 的提供者，所以您可以使用 ActiveX Data 物件 (ADO) 來連接至 ADSI 提供者。
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX 資料物件 ADSI
- ActiveX data object ADSI，使用 ADO 系結至 ADSI 提供者
- 服務提供者 ADSI，使用 ActiveX 資料物件系結至
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020781"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a><span data-ttu-id="7f4ad-106">使用 ActiveX 資料物件系結至 ADSI 提供者</span><span class="sxs-lookup"><span data-stu-id="7f4ad-106">Using an ActiveX Data Object to Bind to ADSI Providers</span></span>

<span data-ttu-id="7f4ad-107">因為 ADSI 也是 OLE DB 的提供者，所以您可以使用 ActiveX Data 物件 (ADO) 來連接至 ADSI 提供者。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-107">Since ADSI is also an OLE DB provider, you can use an ActiveX Data Object (ADO) to connect to ADSI providers.</span></span> <span data-ttu-id="7f4ad-108">與其他 ADO 提供者一樣，若要連接到 OLE DB 提供者，您必須建立新的連線物件，並選擇性地指定認證。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-108">As with other ADO providers, to connect to an OLE DB provider, you must create a new connection object and, optionally, specify the credentials.</span></span> <span data-ttu-id="7f4ad-109">ADSI OLE DB 提供者的名稱是 **ADsDSOObject**。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-109">The name of the ADSI OLE DB provider is **ADsDSOObject**.</span></span>

<span data-ttu-id="7f4ad-110">例如：</span><span class="sxs-lookup"><span data-stu-id="7f4ad-110">For example:</span></span>


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



<span data-ttu-id="7f4ad-111">在先前的範例中，您會代表目前的使用者進行連接。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-111">In the previous example, you are connected on behalf of the current user.</span></span> <span data-ttu-id="7f4ad-112">若要指定不同的認證，請使用連接屬性：</span><span class="sxs-lookup"><span data-stu-id="7f4ad-112">To specify different credentials, use connection properties:</span></span>


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



<span data-ttu-id="7f4ad-113">ADSI OLE DB 定義下列連接屬性。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-113">ADSI OLE DB defines the following connection properties.</span></span>



| <span data-ttu-id="7f4ad-114">屬性</span><span class="sxs-lookup"><span data-stu-id="7f4ad-114">Property</span></span>           | <span data-ttu-id="7f4ad-115">資料類型</span><span class="sxs-lookup"><span data-stu-id="7f4ad-115">Data type</span></span>   | <span data-ttu-id="7f4ad-116">預設</span><span class="sxs-lookup"><span data-stu-id="7f4ad-116">Default</span></span>   |
|--------------------|-------------|-----------|
| <span data-ttu-id="7f4ad-117">「使用者識別碼」</span><span class="sxs-lookup"><span data-stu-id="7f4ad-117">"User ID"</span></span>          | <span data-ttu-id="7f4ad-118">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="7f4ad-118">**BSTR**</span></span>    | <span data-ttu-id="7f4ad-119">**NULL**</span><span class="sxs-lookup"><span data-stu-id="7f4ad-119">**NULL**</span></span>  |
| <span data-ttu-id="7f4ad-120">"Password"</span><span class="sxs-lookup"><span data-stu-id="7f4ad-120">"Password"</span></span>         | <span data-ttu-id="7f4ad-121">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="7f4ad-121">**BSTR**</span></span>    | <span data-ttu-id="7f4ad-122">**NULL**</span><span class="sxs-lookup"><span data-stu-id="7f4ad-122">**NULL**</span></span>  |
| <span data-ttu-id="7f4ad-123">「加密密碼」</span><span class="sxs-lookup"><span data-stu-id="7f4ad-123">"Encrypt Password"</span></span> | <span data-ttu-id="7f4ad-124">**布林**</span><span class="sxs-lookup"><span data-stu-id="7f4ad-124">**BOOLEAN**</span></span> | <span data-ttu-id="7f4ad-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="7f4ad-125">**FALSE**</span></span> |
| <span data-ttu-id="7f4ad-126">"ADSI 旗標"</span><span class="sxs-lookup"><span data-stu-id="7f4ad-126">"ADSI Flag"</span></span>        | <span data-ttu-id="7f4ad-127">**Long**</span><span class="sxs-lookup"><span data-stu-id="7f4ad-127">**Long**</span></span>    | <span data-ttu-id="7f4ad-128">0</span><span class="sxs-lookup"><span data-stu-id="7f4ad-128">0</span></span>         |



 

<span data-ttu-id="7f4ad-129">使用 OLE DB ADO 時，您無法系結至特定的物件。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-129">Using OLE DB ADO, you cannot bind to a specific object.</span></span> <span data-ttu-id="7f4ad-130">不過，您可以查詢特定物件並取回結果集。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-130">You can, however, query a specific object and get a result set back.</span></span> <span data-ttu-id="7f4ad-131">只有支援 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 的 ADSI 提供者才能讓 ADO 成為程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-131">Only ADSI providers that support [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) benefit from having ADO as a programming model.</span></span>

<span data-ttu-id="7f4ad-132">ADSI 旗標屬性是用來指定系結驗證選項。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-132">The ADSI Flag property is used to specify the binding authentication option.</span></span> <span data-ttu-id="7f4ad-133">這個屬性可以是來自 [**ADS \_ 驗證 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) 列舉的旗標組合。</span><span class="sxs-lookup"><span data-stu-id="7f4ad-133">This property can be a combination of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration.</span></span>

 

 




