---
title: 選擇描述性屬性的內容
description: 某些屬性的內容是特定的，而其他屬性的內容則是由伺服器開發人員所提供的描述性文字所組成。
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b77860eaefeb4e371c69fdf6acd205c77d763c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683023"
---
# <a name="choosing-the-content-for-descriptive-properties"></a><span data-ttu-id="1915c-103">選擇描述性屬性的內容</span><span class="sxs-lookup"><span data-stu-id="1915c-103">Choosing the Content for Descriptive Properties</span></span>

<span data-ttu-id="1915c-104">某些屬性的內容是特定的，而其他屬性的內容則是由伺服器開發人員所提供的描述性文字所組成。</span><span class="sxs-lookup"><span data-stu-id="1915c-104">While the content of some properties is specific, the content for other properties consists of descriptive text that is left to the server developer to provide.</span></span> <span data-ttu-id="1915c-105">此外，每個屬性的資訊類型都會根據物件而有所不同。</span><span class="sxs-lookup"><span data-stu-id="1915c-105">Additionally, the type of information for each property varies depending on the object.</span></span> <span data-ttu-id="1915c-106">下表提供選擇這些描述性屬性內容的建議。</span><span class="sxs-lookup"><span data-stu-id="1915c-106">The following table provides suggestions for choosing the content of these descriptive properties.</span></span>



| <span data-ttu-id="1915c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="1915c-107">Property</span></span>                                        | <span data-ttu-id="1915c-108">內容建議</span><span class="sxs-lookup"><span data-stu-id="1915c-108">Content suggestion</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1915c-109">**Name**</span><span class="sxs-lookup"><span data-stu-id="1915c-109">**Name**</span></span>](name-property.md)                   | <span data-ttu-id="1915c-110">此標籤會在其容器內簡短描述和識別物件，例如按下按鈕中的文字、功能表項目的名稱，或是在編輯控制項旁邊顯示的標籤。</span><span class="sxs-lookup"><span data-stu-id="1915c-110">A label that briefly describes and identifies the object within its container, such as the text in a push button, the name of a menu item, or a label displayed next to an edit control.</span></span>                                                                              |
| [<span data-ttu-id="1915c-111">**DefaultAction**</span><span class="sxs-lookup"><span data-stu-id="1915c-111">**DefaultAction**</span></span>](defaultaction-property.md) | <span data-ttu-id="1915c-112">與物件的預設互動。</span><span class="sxs-lookup"><span data-stu-id="1915c-112">The default interaction with the object.</span></span> <span data-ttu-id="1915c-113">這個屬性所傳回的字串是單一動詞，例如，針對工具列按鈕按下 "，或以動詞開頭的簡短片語。</span><span class="sxs-lookup"><span data-stu-id="1915c-113">The string returned by this property is either a single verb, such as "Press" for a toolbar button, or a short phrase that begins with a verb.</span></span>                                                                               |
| [<span data-ttu-id="1915c-114">**值**</span><span class="sxs-lookup"><span data-stu-id="1915c-114">**Value**</span></span>](value-property.md)                 | <span data-ttu-id="1915c-115">物件中包含的資訊，例如編輯控制項中的文字或 HTML 連結的檔案名。</span><span class="sxs-lookup"><span data-stu-id="1915c-115">Information contained in the object, such as the text in an edit control or the file name of an HTML link.</span></span> <span data-ttu-id="1915c-116">[**Value**](value-property.md)屬性的內容可以變更，而 [**Name**](name-property.md)屬性的內容不會變更。</span><span class="sxs-lookup"><span data-stu-id="1915c-116">The contents of the [**Value**](value-property.md) property can change, whereas the contents of the [**Name**](name-property.md) property do not change.</span></span> |
| [<span data-ttu-id="1915c-117">**描述**</span><span class="sxs-lookup"><span data-stu-id="1915c-117">**Description**</span></span>](description-property.md)     | <span data-ttu-id="1915c-118">描述物件的外觀。</span><span class="sxs-lookup"><span data-stu-id="1915c-118">Describes the object's appearance.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="1915c-119">**Help**</span><span class="sxs-lookup"><span data-stu-id="1915c-119">**Help**</span></span>](help-property.md)                   | <span data-ttu-id="1915c-120">工具提示或氣球樣式的資訊，用來描述物件的用途或使用方式。</span><span class="sxs-lookup"><span data-stu-id="1915c-120">Tooltip or balloon-style information used either to describe what the object does or how to use it.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="1915c-121">**HelpTopic**</span><span class="sxs-lookup"><span data-stu-id="1915c-121">**HelpTopic**</span></span>](helptopic-property.md)         | <span data-ttu-id="1915c-122">檔物件之 [WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) 主題的內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="1915c-122">A context identifier of a [WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) topic that documents the object.</span></span>                                                                                                                                                 |



 

<span data-ttu-id="1915c-123">針對 [**角色**](role-property.md)使用其中一個預先定義的 [物件角色](object-roles.md)值，並針對該 [**狀態**](state-property.md)使用適當的 [物件狀態常數](object-state-constants.md)組合。</span><span class="sxs-lookup"><span data-stu-id="1915c-123">Use one of the predefined [object role](object-roles.md) values for the [**Role**](role-property.md) and the appropriate combination of [object state constants](object-state-constants.md) for the [**State**](state-property.md).</span></span>

<span data-ttu-id="1915c-124">自訂控制項的屬性內容必須符合自訂控制項所模擬之系統提供控制項的屬性內容。</span><span class="sxs-lookup"><span data-stu-id="1915c-124">The content of the properties for custom controls must match the content of the properties for the system-provided controls that the custom controls emulate.</span></span> <span data-ttu-id="1915c-125">如需系統提供之控制項所支援之屬性的詳細資訊，請參閱 [附錄 A：支援的消費者介面專案參考](appendix-a--supported-user-interface-elements-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="1915c-125">For information about the properties supported by system-provided controls, see [Appendix A: Supported User Interface Elements Reference](appendix-a--supported-user-interface-elements-reference.md).</span></span>

 

 