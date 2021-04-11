---
description: WriteIniValues 動作會將應用程式所需寫入的 .ini 檔案資訊寫入 .ini 檔案。
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: WriteIniValues 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849932"
---
# <a name="writeinivalues-action"></a><span data-ttu-id="afcf2-103">WriteIniValues 動作</span><span class="sxs-lookup"><span data-stu-id="afcf2-103">WriteIniValues Action</span></span>

<span data-ttu-id="afcf2-104">WriteIniValues 動作會將應用程式所需寫入的 .ini 檔案資訊寫入 .ini 檔案。</span><span class="sxs-lookup"><span data-stu-id="afcf2-104">The WriteIniValues action writes the .ini file information that the application needs written to its .ini files.</span></span> <span data-ttu-id="afcf2-105">這項資訊的寫入是由 [元件資料表](component-table.md)所管制。</span><span class="sxs-lookup"><span data-stu-id="afcf2-105">The writing of this information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="afcf2-106">如果對應的元件已設定為要安裝在本機或從來源執行，則會寫入 .ini 值。</span><span class="sxs-lookup"><span data-stu-id="afcf2-106">An .ini value is written if the corresponding component has been set to be installed either locally or run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="afcf2-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="afcf2-107">Sequence Restrictions</span></span>

<span data-ttu-id="afcf2-108">InstallValidate 動作必須位於 WriteIniValues 動作之前。</span><span class="sxs-lookup"><span data-stu-id="afcf2-108">The InstallValidate action must come before the WriteIniValues action.</span></span> <span data-ttu-id="afcf2-109">如果序列中有 [RemoveIniValues 動作](removeinivalues-action.md) ，則必須在 WriteIniValues 動作之前。</span><span class="sxs-lookup"><span data-stu-id="afcf2-109">If there is a [RemoveIniValues action](removeinivalues-action.md) in the sequence, then it must come before the WriteIniValues action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="afcf2-110">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="afcf2-110">ActionData Messages</span></span>



| <span data-ttu-id="afcf2-111">欄位</span><span class="sxs-lookup"><span data-stu-id="afcf2-111">Field</span></span> | <span data-ttu-id="afcf2-112">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="afcf2-112">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="afcf2-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="afcf2-113">\[1\]</span></span> | <span data-ttu-id="afcf2-114">.Ini 檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="afcf2-114">Identifier of .ini file.</span></span>                |
| <span data-ttu-id="afcf2-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="afcf2-115">\[2\]</span></span> | <span data-ttu-id="afcf2-116">下一節中的 .ini 檔案索引鍵。</span><span class="sxs-lookup"><span data-stu-id="afcf2-116">.ini file key in the following section.</span></span> |
| <span data-ttu-id="afcf2-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="afcf2-117">\[3\]</span></span> | <span data-ttu-id="afcf2-118">從 .ini 檔案移除的專案。</span><span class="sxs-lookup"><span data-stu-id="afcf2-118">Item removed from .ini file.</span></span>            |
| <span data-ttu-id="afcf2-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="afcf2-119">\[4\]</span></span> | <span data-ttu-id="afcf2-120">從 .ini 檔案中移除的值。</span><span class="sxs-lookup"><span data-stu-id="afcf2-120">Value removed from .ini file.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="afcf2-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="afcf2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afcf2-122">IniFile 資料表</span><span class="sxs-lookup"><span data-stu-id="afcf2-122">IniFile table</span></span>](inifile-table.md)
</dt> </dl>

 

 



