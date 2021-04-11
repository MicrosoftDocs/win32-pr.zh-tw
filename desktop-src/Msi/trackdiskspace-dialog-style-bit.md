---
description: 如果設定此位，對話方塊會定期呼叫安裝程式。
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: TrackDiskSpace 對話方塊樣式位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111993"
---
# <a name="trackdiskspace-dialog-style-bit"></a><span data-ttu-id="0f4e6-103">TrackDiskSpace 對話方塊樣式位</span><span class="sxs-lookup"><span data-stu-id="0f4e6-103">TrackDiskSpace Dialog Style Bit</span></span>

<span data-ttu-id="0f4e6-104">如果設定此位，對話方塊會定期呼叫安裝程式。</span><span class="sxs-lookup"><span data-stu-id="0f4e6-104">If this bit is set, the dialog box periodically calls the installer.</span></span> <span data-ttu-id="0f4e6-105">如果屬性變更，則會通知對話方塊上的控制項。</span><span class="sxs-lookup"><span data-stu-id="0f4e6-105">If the property changes, it notifies the controls on the dialog.</span></span> <span data-ttu-id="0f4e6-106">如果對話方塊上有控制項指出磁碟空間，則可以使用這個樣式。</span><span class="sxs-lookup"><span data-stu-id="0f4e6-106">This style can be used if there is a control on the dialog indicating disk space.</span></span> <span data-ttu-id="0f4e6-107">如果使用者切換到另一個應用程式、新增或移除檔案，或修改可用的磁碟空間，您可以使用此樣式快速執行變更。</span><span class="sxs-lookup"><span data-stu-id="0f4e6-107">If the user switches to another application, adds or removes files, or otherwise modifies available disk space, you can quickly implement the change using this style.</span></span>

<span data-ttu-id="0f4e6-108">任何依賴 [**OutOfDiskSpace**](outofdiskspace.md) 屬性來判斷是否要顯示對話方塊的對話方塊都必須設定對話方塊的 TrackDiskSpace 對話方塊樣式位，以動態更新目標磁片區上的空間。</span><span class="sxs-lookup"><span data-stu-id="0f4e6-108">Any dialog box relying on the [**OutOfDiskSpace**](outofdiskspace.md) property to determine whether to bring up a dialog must set the TrackDiskSpace Dialog Style Bit for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="value"></a><span data-ttu-id="0f4e6-109">值</span><span class="sxs-lookup"><span data-stu-id="0f4e6-109">Value</span></span>



| <span data-ttu-id="0f4e6-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="0f4e6-110">Decimal</span></span> | <span data-ttu-id="0f4e6-111">十六進位</span><span class="sxs-lookup"><span data-stu-id="0f4e6-111">Hexadecimal</span></span> | <span data-ttu-id="0f4e6-112">常數</span><span class="sxs-lookup"><span data-stu-id="0f4e6-112">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="0f4e6-113">32</span><span class="sxs-lookup"><span data-stu-id="0f4e6-113">32</span></span>      | <span data-ttu-id="0f4e6-114">0x00000020</span><span class="sxs-lookup"><span data-stu-id="0f4e6-114">0x00000020</span></span>  | <span data-ttu-id="0f4e6-115">**msidbDialogAttributesTrackDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="0f4e6-115">**msidbDialogAttributesTrackDiskSpace**</span></span> |



 

 

 



