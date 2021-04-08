---
title: 建立外部參考
description: 如果已建立外部交叉參考物件，且網域控制站使用它來產生參考，則交叉參考物件會在下列屬性中提供兩個重要的資料元素。
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- 外部參考 Active Directory
- Active Directory 範例 Active Directory，建立外部參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681680"
---
# <a name="creating-an-external-referral"></a><span data-ttu-id="9ab59-105">建立外部參考</span><span class="sxs-lookup"><span data-stu-id="9ab59-105">Creating an External Referral</span></span>

<span data-ttu-id="9ab59-106">如果已建立外部 [**交叉**](/windows/desktop/ADSchema/c-crossref) 參考物件，且網域控制站使用它來產生參考，則 **交叉** 參考物件會在下列屬性中提供兩個重要的資料元素。</span><span class="sxs-lookup"><span data-stu-id="9ab59-106">If an external [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is created and a domain controller uses it to generate a referral, the **crossRef** object provides two important data elements in the following properties.</span></span> <span data-ttu-id="9ab59-107">如需可能發生這種情況的詳細資訊，請參閱上一節。</span><span class="sxs-lookup"><span data-stu-id="9ab59-107">For more information about situations where this can occur, see the previous section.</span></span>



| <span data-ttu-id="9ab59-108">屬性</span><span class="sxs-lookup"><span data-stu-id="9ab59-108">Property</span></span>                           | <span data-ttu-id="9ab59-109">描述</span><span class="sxs-lookup"><span data-stu-id="9ab59-109">Description</span></span>                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ab59-110">**dnsRoot**</span><span class="sxs-lookup"><span data-stu-id="9ab59-110">**dnsRoot**</span></span>](/windows/desktop/ADSchema/a-dnsroot) | <span data-ttu-id="9ab59-111">指定伺服器或網域，該伺服器或網域可以提供 [**nCName**](/windows/desktop/ADSchema/a-ncname)中指定之命名內容的資料。</span><span class="sxs-lookup"><span data-stu-id="9ab59-111">Specifies the server or domain that can serve data from the naming context specified in [**nCName**](/windows/desktop/ADSchema/a-ncname).</span></span>                                           |
| [<span data-ttu-id="9ab59-112">**nCName**</span><span class="sxs-lookup"><span data-stu-id="9ab59-112">**nCName**</span></span>](/windows/desktop/ADSchema/a-ncname)   | <span data-ttu-id="9ab59-113">指定根于 [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)所指定的伺服器或網域之網域、架構或設定容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="9ab59-113">Specifies the distinguished name for the domain, schema, or configuration container rooted at the server or domain specified by [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot).</span></span> |



 

<span data-ttu-id="9ab59-114">例如，如果 DNS 位址為 serv1.northwest.Fabrikam.com 的伺服器提供根目錄為 CN = MyContainer，OU = MyDOM，O = Fabrikam 的命名內容，請將 [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) 設定為該伺服器的 DNS 位址，並將 [**nCName**](/windows/desktop/ADSchema/a-ncname) 設定為網域、架構或設定容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="9ab59-114">For example, if the server with DNS address of serv1.northwest.Fabrikam.com serves the naming context rooted at CN=MyContainer,OU=MyDOM,O=Fabrikam, set the [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) to that server's DNS address and the [**nCName**](/windows/desktop/ADSchema/a-ncname) to the distinguished name of the domain, schema, or configuration container.</span></span>

<span data-ttu-id="9ab59-115">如需詳細資訊和顯示如何建立外部參考的程式碼範例，請參閱 [建立外部交叉參考物件的範例程式碼](example-code-for-creating-an-external-crossref-object.md)。</span><span class="sxs-lookup"><span data-stu-id="9ab59-115">For more information and a code example that shows how to create an external referral, see [Example Code for Creating an External crossRef Object](example-code-for-creating-an-external-crossref-object.md).</span></span>

 

 