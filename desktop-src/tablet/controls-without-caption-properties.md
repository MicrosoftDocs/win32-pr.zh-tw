---
description: 針對 Tablet PC 使用沒有標題屬性之控制項的簡介。
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: 沒有 Caption 屬性的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510756"
---
# <a name="controls-without-caption-properties"></a><span data-ttu-id="7a6f3-103">沒有 Caption 屬性的控制項</span><span class="sxs-lookup"><span data-stu-id="7a6f3-103">Controls Without Caption Properties</span></span>

<span data-ttu-id="7a6f3-104">當控制項沒有自己的標題屬性時，請採取下列步驟來確保協助工具輔助可識別控制項：</span><span class="sxs-lookup"><span data-stu-id="7a6f3-104">When a control does not have its own caption property, take the following steps to ensure that accessibility aids can identify the controls:</span></span>

-   <span data-ttu-id="7a6f3-105">建立具有有意義和描述性名稱的靜態文字控制項。</span><span class="sxs-lookup"><span data-stu-id="7a6f3-105">Create a static text control with a meaningful and descriptive name.</span></span>
-   <span data-ttu-id="7a6f3-106">將靜態標籤放在參考的控制項上方（依 tab 順序）。</span><span class="sxs-lookup"><span data-stu-id="7a6f3-106">Place the static label so it immediately precedes the referenced control, in tab order.</span></span>
-   <span data-ttu-id="7a6f3-107">確定標籤文字的結尾是冒號，例如 "Settings："</span><span class="sxs-lookup"><span data-stu-id="7a6f3-107">Ensure that the label text ends with a colon, for example, "Settings:"</span></span>
-   <span data-ttu-id="7a6f3-108">將標籤文字緊接在參考的控制項左方或前面。</span><span class="sxs-lookup"><span data-stu-id="7a6f3-108">Position the label text immediately to the left or preceding the referenced control.</span></span>
-   <span data-ttu-id="7a6f3-109">如果不適合以視覺化方式顯示靜態文字，請將其設為隱藏。</span><span class="sxs-lookup"><span data-stu-id="7a6f3-109">Make the static text invisible if it is not appropriate to display it visually.</span></span> <span data-ttu-id="7a6f3-110">若要這麼做，請在資源腳本中指派適當的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a6f3-110">Do this by assigning the appropriate attribute in the resource script.</span></span> <span data-ttu-id="7a6f3-111">當控制項的名稱或函式是透過靜態文字控制項（例如圖形或相關的選項按鈕）來以視覺化方式提供時，這可能會很適合。</span><span class="sxs-lookup"><span data-stu-id="7a6f3-111">This may be appropriate when the name or function of a control is visually provided by means other than static text control, such as a graphic or a related radio button.</span></span>

<span data-ttu-id="7a6f3-112">靜態控制項的適當使用方式，是針對沒有內建標籤的控制項正確地執行加上底線的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="7a6f3-112">The proper use of static controls is the only way to correctly implement underlined access keys for controls that do not have intrinsic labels.</span></span> <span data-ttu-id="7a6f3-113">如需使用沒有標題屬性之控制項的詳細資訊，請參閱 [協助工具](/windows/desktop/accessibility) 一節。</span><span class="sxs-lookup"><span data-stu-id="7a6f3-113">For more information about using controls that do not have caption properties, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
