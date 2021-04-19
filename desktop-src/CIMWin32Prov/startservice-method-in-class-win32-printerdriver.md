---
description: StartService 方法會將服務置於啟動狀態。
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: Win32_PrinterDriver 類別的 StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44e6fedb9e1d0edd9f355c654c7fe2cd25760ec7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991641"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="4c505-103">Win32 PrinterDriver 類別的 StartService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4c505-103">StartService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="4c505-104">**StartService** 方法會將服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="4c505-104">The **StartService** method places the service in the started state.</span></span>

<span data-ttu-id="4c505-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="4c505-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4c505-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="4c505-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c505-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c505-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="4c505-108">參數</span><span class="sxs-lookup"><span data-stu-id="4c505-108">Parameters</span></span>

<span data-ttu-id="4c505-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4c505-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c505-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c505-110">Return value</span></span>

<span data-ttu-id="4c505-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c505-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="4c505-112">針對不同于下列清單中所列的值，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants)。</span><span class="sxs-lookup"><span data-stu-id="4c505-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="4c505-113">**0**</span><span class="sxs-lookup"><span data-stu-id="4c505-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4c505-114">服務已成功啟動。</span><span class="sxs-lookup"><span data-stu-id="4c505-114">Service successfully started.</span></span>

</dd> <dt>

<span data-ttu-id="4c505-115">**1**</span><span class="sxs-lookup"><span data-stu-id="4c505-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="4c505-116">不支援要求。</span><span class="sxs-lookup"><span data-stu-id="4c505-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c505-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c505-117">Requirements</span></span>



| <span data-ttu-id="4c505-118">需求</span><span class="sxs-lookup"><span data-stu-id="4c505-118">Requirement</span></span> | <span data-ttu-id="4c505-119">值</span><span class="sxs-lookup"><span data-stu-id="4c505-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c505-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c505-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4c505-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c505-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="4c505-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c505-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4c505-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c505-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="4c505-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c505-124">Namespace</span></span><br/>                | <span data-ttu-id="4c505-125">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4c505-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="4c505-126">MOF</span><span class="sxs-lookup"><span data-stu-id="4c505-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c505-127"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c505-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c505-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4c505-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c505-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c505-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="4c505-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c505-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c505-131">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4c505-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4c505-132">**Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="4c505-132">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

