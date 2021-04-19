---
description: 停止收集器。 如果收集器是以服務方式執行，則停止服務是較佳的方法。
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Control 類別的 Shutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d401ac528498d7b8ab5ccacbf6a0b5bf781555f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970520"
---
# <a name="shutdown-method-of-the-control-class"></a><span data-ttu-id="3d3a2-104">Control 類別的 Shutdown 方法</span><span class="sxs-lookup"><span data-stu-id="3d3a2-104">Shutdown method of the Control class</span></span>

<span data-ttu-id="3d3a2-105">停止收集器。</span><span class="sxs-lookup"><span data-stu-id="3d3a2-105">Stops the collector.</span></span> <span data-ttu-id="3d3a2-106">如果收集器是以服務方式執行，則停止服務是較佳的方法。</span><span class="sxs-lookup"><span data-stu-id="3d3a2-106">If the collector is running as a service, stopping the service is the better approach.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3a2-107">語法</span><span class="sxs-lookup"><span data-stu-id="3d3a2-107">Syntax</span></span>


```mof
void Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="3d3a2-108">參數</span><span class="sxs-lookup"><span data-stu-id="3d3a2-108">Parameters</span></span>

<span data-ttu-id="3d3a2-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3d3a2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d3a2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d3a2-110">Return value</span></span>

<span data-ttu-id="3d3a2-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3d3a2-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d3a2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d3a2-112">Requirements</span></span>



| <span data-ttu-id="3d3a2-113">需求</span><span class="sxs-lookup"><span data-stu-id="3d3a2-113">Requirement</span></span> | <span data-ttu-id="3d3a2-114">值</span><span class="sxs-lookup"><span data-stu-id="3d3a2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3a2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d3a2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3d3a2-116">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d3a2-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3d3a2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d3a2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3d3a2-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3d3a2-118">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="3d3a2-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="3d3a2-119">Namespace</span></span><br/>                | <span data-ttu-id="3d3a2-120">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="3d3a2-120">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="3d3a2-121">MOF</span><span class="sxs-lookup"><span data-stu-id="3d3a2-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d3a2-122"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d3a2-122"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d3a2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3d3a2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d3a2-124"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3d3a2-124"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3d3a2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d3a2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3a2-126">**控制**</span><span class="sxs-lookup"><span data-stu-id="3d3a2-126">**Control**</span></span>](control.md)
</dt> </dl>

 

 




