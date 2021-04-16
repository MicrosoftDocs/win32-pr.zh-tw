---
description: 使用 Microsoft Windows 對話方塊時，您必須為所有控制項加上標籤，以加速語音功能。 [下列執行] 對話方塊會顯示下拉式清單方塊的靜態文字控制項標籤。 靜態文字的結尾是冒號。
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: 在對話方塊中命名控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553522"
---
# <a name="naming-controls-in-dialog-boxes"></a><span data-ttu-id="8c330-105">在對話方塊中命名控制項</span><span class="sxs-lookup"><span data-stu-id="8c330-105">Naming Controls in Dialog Boxes</span></span>

<span data-ttu-id="8c330-106">使用 Microsoft Windows 對話方塊時，您必須為所有控制項加上標籤，以加速語音功能。</span><span class="sxs-lookup"><span data-stu-id="8c330-106">When using Microsoft Windows dialog boxes, you must label all controls to facilitate speech functionality.</span></span> <span data-ttu-id="8c330-107">[下列 **執行** ] 對話方塊會顯示下拉式清單方塊的靜態文字控制項標籤。</span><span class="sxs-lookup"><span data-stu-id="8c330-107">The following **Run** dialog box shows a static text control label for a drop-down list box.</span></span> <span data-ttu-id="8c330-108">靜態文字的結尾是冒號。</span><span class="sxs-lookup"><span data-stu-id="8c330-108">Static text ends with a colon.</span></span>

![顯示 [執行] 對話方塊的螢幕擷取畫面](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

<span data-ttu-id="8c330-110">控制項分為兩種：</span><span class="sxs-lookup"><span data-stu-id="8c330-110">There are two types of controls:</span></span>

-   <span data-ttu-id="8c330-111">控制項，其標題為控制項的屬性，例如命令按鈕和核取方塊。</span><span class="sxs-lookup"><span data-stu-id="8c330-111">Controls that have their captions as a property of that control, such as command buttons and check boxes.</span></span> <span data-ttu-id="8c330-112">只要標題定義正確，協助工具協助工具就無法識別這些控制項。</span><span class="sxs-lookup"><span data-stu-id="8c330-112">Accessibility aids have no trouble identifying these controls as long as the caption is properly defined.</span></span>
-   <span data-ttu-id="8c330-113">沒有專屬標題的控制項（例如編輯控制項、清單方塊和清單視圖）必須使用不同的靜態文字控制項來標記。</span><span class="sxs-lookup"><span data-stu-id="8c330-113">Controls that do not have their own captions, such as edit controls, list boxes and list views, must be labeled by using separate static text controls.</span></span> <span data-ttu-id="8c330-114">如需沒有專屬標題之控制項的詳細資訊，請參閱 [沒有標題屬性的控制項](controls-without-caption-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="8c330-114">For more information about controls that do not have their own captions, see [Controls Without Caption Properties](controls-without-caption-properties.md).</span></span>

<span data-ttu-id="8c330-115">您可以使用數種技術來克服控制項沒有自己的標題的情況，但只有在標準對話方塊管理員 (SDM) 所顯示的視窗中才有效。</span><span class="sxs-lookup"><span data-stu-id="8c330-115">Several techniques can be used to overcome situations in which controls do not have their own captions, but they are only effective for windows that are displayed by the Standard Dialog Manager (SDM).</span></span> <span data-ttu-id="8c330-116">所有其他視窗都需要明確支援 Microsoft Active Accessibility，以公開控制項之間的名稱和關聯性。</span><span class="sxs-lookup"><span data-stu-id="8c330-116">All other windows need to expose the names and relationship between controls by explicitly supporting Microsoft Active Accessibility.</span></span> <span data-ttu-id="8c330-117">如需 Active Accessibility 的詳細資訊，請參閱 MSDN Library 的 [協助工具](/windows/desktop/accessibility) 一節。</span><span class="sxs-lookup"><span data-stu-id="8c330-117">For more information about Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section of the MSDN Library.</span></span>

 

 
