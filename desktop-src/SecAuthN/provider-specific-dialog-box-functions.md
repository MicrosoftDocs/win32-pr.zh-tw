---
description: 提供者特定的對話方塊函式可讓提供者藉由變更系統對話方塊或顯示自訂對話方塊，來顯示及處理網路特定的資訊。
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Provider-Specific 對話方塊函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980614"
---
# <a name="provider-specific-dialog-box-functions"></a><span data-ttu-id="6dbf1-103">Provider-Specific 對話方塊函數</span><span class="sxs-lookup"><span data-stu-id="6dbf1-103">Provider-Specific Dialog Box Functions</span></span>

<span data-ttu-id="6dbf1-104">提供者特定的對話方塊函式可讓提供者藉由變更系統對話方塊或顯示自訂對話方塊，來顯示及處理網路特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-104">Provider-specific dialog box functions enable a provider to display and handle network-specific information by altering system dialog boxes or displaying custom dialog boxes.</span></span>

<span data-ttu-id="6dbf1-105">下列對話方塊功能會將按鈕新增至 [檔案管理員 **屬性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-105">The following dialog box functions add buttons to the File Manager **Properties** dialog box.</span></span> <span data-ttu-id="6dbf1-106">然後，提供者可以處理這些按鈕的事件，以執行網路特定的工作。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-106">The provider can then handle the events of those buttons to perform network-specific tasks.</span></span> <span data-ttu-id="6dbf1-107">請注意，可加入的按鈕數目有限制。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-107">Note that there is a limit to the number of buttons that can be added.</span></span> <span data-ttu-id="6dbf1-108">因此，提供者應該謹慎使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-108">Because of this, providers should use this capability sparingly.</span></span> <span data-ttu-id="6dbf1-109">此外，提供者可能會發現自己無法加入按鈕，因為其他提供者已經使用了可用的空間。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-109">Also, a provider may find itself unable to add a button because the available space has been used already by other providers.</span></span> <span data-ttu-id="6dbf1-110">網路提供者應該會處理這種情況。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-110">A network provider should handle this situation.</span></span>



| <span data-ttu-id="6dbf1-111">函式</span><span class="sxs-lookup"><span data-stu-id="6dbf1-111">Function</span></span>                                           | <span data-ttu-id="6dbf1-112">描述</span><span class="sxs-lookup"><span data-stu-id="6dbf1-112">Description</span></span>                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dbf1-113">**NPGetPropertyText**</span><span class="sxs-lookup"><span data-stu-id="6dbf1-113">**NPGetPropertyText**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | <span data-ttu-id="6dbf1-114">決定針對特定資源新增至屬性對話方塊的按鈕名稱。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-114">Determines the names of buttons added to a property dialog box for a specific resource.</span></span><br/>                                      |
| [<span data-ttu-id="6dbf1-115">**NPPropertyDialog**</span><span class="sxs-lookup"><span data-stu-id="6dbf1-115">**NPPropertyDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | <span data-ttu-id="6dbf1-116">當使用者按一下使用 [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) 函式加入的按鈕時呼叫。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-116">Called when a user clicks a button added by using the [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) function.</span></span><br/>               |
| [<span data-ttu-id="6dbf1-117">**NPSearchDialog**</span><span class="sxs-lookup"><span data-stu-id="6dbf1-117">**NPSearchDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | <span data-ttu-id="6dbf1-118">可讓網路提供者在 **連接** 對話方塊中所提供的以外，執行自己的搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-118">Enables network providers to implement their own search functionality beyond that provided in the **Connection** dialog box.</span></span><br/> |
| [<span data-ttu-id="6dbf1-119">**NPFormatNetworkName**</span><span class="sxs-lookup"><span data-stu-id="6dbf1-119">**NPFormatNetworkName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | <span data-ttu-id="6dbf1-120">可讓網路提供者在將網路名稱呈現給使用者之前，先將其格式化或修改。</span><span class="sxs-lookup"><span data-stu-id="6dbf1-120">Enables network providers to format or otherwise modify network names before they are presented to the user.</span></span><br/>                 |



 

 

 




