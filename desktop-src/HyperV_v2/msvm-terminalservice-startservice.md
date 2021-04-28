---
description: Msvm_TerminalService 類別的 StartService 方法會啟動服務。
ms.assetid: 499e4650-255f-4c84-98fc-de81d5cd6daf
title: Msvm_TerminalService 類別的 StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 33d7bddc012e7f51042950f093a84a09723e7bd8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109506"
---
# <a name="startservice-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="56cd8-103">Msvm TerminalService 類別的 StartService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="56cd8-103">StartService method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="56cd8-104">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="56cd8-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="56cd8-105">語法</span><span class="sxs-lookup"><span data-stu-id="56cd8-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="56cd8-106">參數</span><span class="sxs-lookup"><span data-stu-id="56cd8-106">Parameters</span></span>

<span data-ttu-id="56cd8-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="56cd8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56cd8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="56cd8-108">Return value</span></span>

<span data-ttu-id="56cd8-109">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="56cd8-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="56cd8-110">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="56cd8-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="56cd8-111">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="56cd8-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="56cd8-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="56cd8-112">Requirements</span></span>



| <span data-ttu-id="56cd8-113">需求</span><span class="sxs-lookup"><span data-stu-id="56cd8-113">Requirement</span></span> | <span data-ttu-id="56cd8-114">值</span><span class="sxs-lookup"><span data-stu-id="56cd8-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56cd8-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56cd8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="56cd8-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="56cd8-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="56cd8-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56cd8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="56cd8-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="56cd8-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="56cd8-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="56cd8-119">Namespace</span></span><br/>                | <span data-ttu-id="56cd8-120">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="56cd8-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="56cd8-121">MOF</span><span class="sxs-lookup"><span data-stu-id="56cd8-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56cd8-122"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="56cd8-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56cd8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="56cd8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56cd8-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56cd8-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56cd8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56cd8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56cd8-126">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="56cd8-126">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




