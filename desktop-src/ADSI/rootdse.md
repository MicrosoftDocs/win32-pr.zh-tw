---
title: 'RootDSE (ADSI) '
description: 每部目錄伺服器都有一個稱為 RootDSE 的唯一專案。 它會提供伺服器的相關資料，例如其功能、支援的 LDAP 版本，以及它所使用的命名內容。
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683093"
---
# <a name="rootdse-adsi"></a><span data-ttu-id="ebb45-104">RootDSE (ADSI) </span><span class="sxs-lookup"><span data-stu-id="ebb45-104">RootDSE (ADSI)</span></span>

<span data-ttu-id="ebb45-105">每部目錄伺服器都有一個稱為 **RootDSE** 的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="ebb45-105">Each directory server has a unique entry called **RootDSE**.</span></span> <span data-ttu-id="ebb45-106">它會提供伺服器的相關資料，例如其功能、支援的 LDAP 版本，以及它所使用的命名內容。</span><span class="sxs-lookup"><span data-stu-id="ebb45-106">It provides data about the server, such as its capabilities, the LDAP version it supports, and the naming contexts it uses.</span></span>

<span data-ttu-id="ebb45-107">例如，建立可在任何 Windows 網域環境執行的腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="ebb45-107">For example, to create a script, or application, that can run on any Windows domain environment.</span></span> <span data-ttu-id="ebb45-108">您可以在連接到 Active Directory 時指定辨別名稱、伺服器名稱或功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="ebb45-108">You can specify either the distinguished name, server name, or domain name when connecting to Active Directory.</span></span> <span data-ttu-id="ebb45-109">如果您沒有此資訊，您可以接著使用 **RootDSE** 物件來建立連接。</span><span class="sxs-lookup"><span data-stu-id="ebb45-109">If you do not have this information, you can then use the **RootDSE** object to establish a connection.</span></span> <span data-ttu-id="ebb45-110">下列程式碼範例會變更任何網域中的網域描述。</span><span class="sxs-lookup"><span data-stu-id="ebb45-110">The following code example changes the domain description in any domain.</span></span>


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



<span data-ttu-id="ebb45-111">藉由從 **RootDSE** 取得 **defaultNamingCoNtext** 屬性，您可以系結至目前的網域，例如 fabrikam **defaultNamingCoNtext** 是 DC = Fabrikam，DC = COM。</span><span class="sxs-lookup"><span data-stu-id="ebb45-111">By getting the **defaultNamingContext** attribute from **RootDSE**, you can bind to the current domain, for example, the Fabrikam **defaultNamingContext** is DC=Fabrikam, DC=COM.</span></span>

<span data-ttu-id="ebb45-112">若要列舉 **RootDSE** 的屬性，請使用 [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) 介面。</span><span class="sxs-lookup"><span data-stu-id="ebb45-112">To enumerate the properties of the **RootDSE**, use the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface.</span></span> <span data-ttu-id="ebb45-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 不能用於這項工作。</span><span class="sxs-lookup"><span data-stu-id="ebb45-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) cannot be used for this task.</span></span>

<span data-ttu-id="ebb45-114">如需詳細資訊，請參閱 [無伺服器系結和 RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse)。</span><span class="sxs-lookup"><span data-stu-id="ebb45-114">For more information, see [Serverless Binding and RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span></span>

 

 