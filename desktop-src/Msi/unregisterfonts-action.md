---
description: UnregisterFonts 動作會從系統中移除已安裝字型的註冊資訊。
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: UnregisterFonts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982096"
---
# <a name="unregisterfonts-action"></a><span data-ttu-id="f8de8-103">UnregisterFonts 動作</span><span class="sxs-lookup"><span data-stu-id="f8de8-103">UnregisterFonts Action</span></span>

<span data-ttu-id="f8de8-104">UnregisterFonts 動作會從系統中移除已安裝字型的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="f8de8-104">The UnregisterFonts action removes registration information about installed fonts from the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f8de8-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="f8de8-105">Sequence Restrictions</span></span>

<span data-ttu-id="f8de8-106">您必須在 UnregisterFonts 之後呼叫 [RemoveFiles](removefiles-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="f8de8-106">The [RemoveFiles](removefiles-action.md) action must be called after UnregisterFonts.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f8de8-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="f8de8-107">ActionData Messages</span></span>



| <span data-ttu-id="f8de8-108">欄位</span><span class="sxs-lookup"><span data-stu-id="f8de8-108">Field</span></span> | <span data-ttu-id="f8de8-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="f8de8-109">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="f8de8-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f8de8-110">\[1\]</span></span> | <span data-ttu-id="f8de8-111">字型檔。</span><span class="sxs-lookup"><span data-stu-id="f8de8-111">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="f8de8-112">備註</span><span class="sxs-lookup"><span data-stu-id="f8de8-112">Remarks</span></span>

<span data-ttu-id="f8de8-113">如果字型資料表的 File 資料行中指定的檔案 \_ 屬於正在卸載的[](font-table.md)元件，則會執行 UnregisterFonts 動作。</span><span class="sxs-lookup"><span data-stu-id="f8de8-113">The UnregisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being uninstalled.</span></span>

 

 



