---
description: RegisterFonts 動作會向系統註冊已安裝的字型。 此動作會將字型資料表的 FontTitle 資料行中的字型名稱對應到所安裝字型檔案的路徑。
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: RegisterFonts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993121"
---
# <a name="registerfonts-action"></a><span data-ttu-id="92d88-104">RegisterFonts 動作</span><span class="sxs-lookup"><span data-stu-id="92d88-104">RegisterFonts Action</span></span>

<span data-ttu-id="92d88-105">RegisterFonts 動作會向系統註冊已安裝的字型。</span><span class="sxs-lookup"><span data-stu-id="92d88-105">The RegisterFonts action registers installed fonts with the system.</span></span> <span data-ttu-id="92d88-106">此動作會將 [字型資料表](font-table.md) 的 FontTitle 資料行中的字型名稱對應到所安裝字型檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="92d88-106">This action maps the font name in the FontTitle column of the [Font table](font-table.md) to the path of the font file installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="92d88-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="92d88-107">Sequence Restrictions</span></span>

<span data-ttu-id="92d88-108">呼叫 RegisterFonts 動作之前，必須先呼叫 [InstallFiles](installfiles-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="92d88-108">The [InstallFiles](installfiles-action.md) action must be called before calling the RegisterFonts action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="92d88-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="92d88-109">ActionData Messages</span></span>



| <span data-ttu-id="92d88-110">欄位</span><span class="sxs-lookup"><span data-stu-id="92d88-110">Field</span></span> | <span data-ttu-id="92d88-111">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="92d88-111">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="92d88-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="92d88-112">\[1\]</span></span> | <span data-ttu-id="92d88-113">字型檔。</span><span class="sxs-lookup"><span data-stu-id="92d88-113">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="92d88-114">備註</span><span class="sxs-lookup"><span data-stu-id="92d88-114">Remarks</span></span>

<span data-ttu-id="92d88-115">如果字型資料表的 File 資料行中指定的檔案 \_ 屬於正在安裝的[](font-table.md)元件，則會執行 RegisterFonts 動作。</span><span class="sxs-lookup"><span data-stu-id="92d88-115">The RegisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being installed.</span></span>

 

 



