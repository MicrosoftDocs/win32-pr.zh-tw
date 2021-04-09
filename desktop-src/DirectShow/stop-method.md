---
description: Stop 方法會停止播放。
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: '停止方法 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944892"
---
# <a name="stop-method-directshow"></a><span data-ttu-id="315b2-103">停止方法 (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="315b2-103">Stop Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="315b2-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="315b2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="315b2-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="315b2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="315b2-106">`Stop`方法會停止播放。</span><span class="sxs-lookup"><span data-stu-id="315b2-106">The `Stop` method stops playback.</span></span>

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a><span data-ttu-id="315b2-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="315b2-107">Return Value</span></span>

<span data-ttu-id="315b2-108">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="315b2-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="315b2-109">備註</span><span class="sxs-lookup"><span data-stu-id="315b2-109">Remarks</span></span>

<span data-ttu-id="315b2-110">如果 [**EnableResetOnStop**](enableresetonstop-property.md) 設定為 true，則呼叫會將 DVD 導覽和 `Stop` 篩選圖形的其餘部分放入已停止的狀態，這表示當使用者下一次按下 [ **播放** ] 按鈕時，播放會從光碟開頭開始播放。如果 **EnableResetOnStop** 設為 true，當使用者發出下一個 **Play** 命令時，播放會從中斷處繼續進行。</span><span class="sxs-lookup"><span data-stu-id="315b2-110">If [**EnableResetOnStop**](enableresetonstop-property.md) is set to true, calling `Stop` puts the DVD Navigator, along with the rest of the filter graph, into a stopped state, which means that the next time the user presses the **Play** button, playback starts at the beginning of the disc. If **EnableResetOnStop** is set to true, playback resumes where it left off when the user issues the next **Play** command.</span></span>

 

 



