---
description: 快速停止收集器，並捨棄所有已排入佇列的資料。
ms.assetid: 9d96a94b-21ae-40bd-9c7f-b466ca38dce3
ms.tgt_platform: multiple
title: Control 類別的 FastShutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.FastShutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 444fe9c94e9fd247e5976fd67a43b0a5eee8b591
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973369"
---
# <a name="fastshutdown-method-of-the-control-class"></a><span data-ttu-id="7fcbf-103">Control 類別的 FastShutdown 方法</span><span class="sxs-lookup"><span data-stu-id="7fcbf-103">FastShutdown method of the Control class</span></span>

<span data-ttu-id="7fcbf-104">快速停止收集器，並捨棄所有已排入佇列的資料。</span><span class="sxs-lookup"><span data-stu-id="7fcbf-104">Stop the collector quickly, discarding all the queued data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fcbf-105">語法</span><span class="sxs-lookup"><span data-stu-id="7fcbf-105">Syntax</span></span>


```mof
void FastShutdown();
```



## <a name="parameters"></a><span data-ttu-id="7fcbf-106">參數</span><span class="sxs-lookup"><span data-stu-id="7fcbf-106">Parameters</span></span>

<span data-ttu-id="7fcbf-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7fcbf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fcbf-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fcbf-108">Return value</span></span>

<span data-ttu-id="7fcbf-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7fcbf-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcbf-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fcbf-110">Requirements</span></span>



| <span data-ttu-id="7fcbf-111">需求</span><span class="sxs-lookup"><span data-stu-id="7fcbf-111">Requirement</span></span> | <span data-ttu-id="7fcbf-112">值</span><span class="sxs-lookup"><span data-stu-id="7fcbf-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcbf-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fcbf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcbf-114">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fcbf-114">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7fcbf-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fcbf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcbf-116">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7fcbf-116">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="7fcbf-117">命名空間</span><span class="sxs-lookup"><span data-stu-id="7fcbf-117">Namespace</span></span><br/>                | <span data-ttu-id="7fcbf-118">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="7fcbf-118">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="7fcbf-119">MOF</span><span class="sxs-lookup"><span data-stu-id="7fcbf-119">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fcbf-120"><dt>BootEventCollectorWMI Mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fcbf-120"><dt>BootEventCollectorWMI.Mof</dt></span></span> </dl> |
| <span data-ttu-id="7fcbf-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7fcbf-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fcbf-122"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7fcbf-122"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7fcbf-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fcbf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcbf-124">**控制**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-124">**Control**</span></span>](control.md)
</dt> </dl>

 

 




