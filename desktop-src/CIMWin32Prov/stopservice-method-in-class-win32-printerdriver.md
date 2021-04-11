---
description: 將 Win32 PrinterDriver 物件所代表的服務置於 \_ 已停止狀態。
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: 'Win32_PrinterDriver 類別的 StopService 方法 (Sdoias) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025929"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="eee44-103">Win32 PrinterDriver 類別的 StopService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="eee44-103">StopService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="eee44-104">**StopService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將 [**Win32 \_ PrinterDriver**](win32-printerdriver.md)物件所代表的服務放在已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="eee44-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_PrinterDriver**](win32-printerdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="eee44-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="eee44-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eee44-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="eee44-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eee44-107">語法</span><span class="sxs-lookup"><span data-stu-id="eee44-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="eee44-108">參數</span><span class="sxs-lookup"><span data-stu-id="eee44-108">Parameters</span></span>

<span data-ttu-id="eee44-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="eee44-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eee44-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="eee44-110">Return value</span></span>

<span data-ttu-id="eee44-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="eee44-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="eee44-112">針對不同于下列清單中所列的值，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants)。</span><span class="sxs-lookup"><span data-stu-id="eee44-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="eee44-113">**0**</span><span class="sxs-lookup"><span data-stu-id="eee44-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="eee44-114">服務已成功停止。</span><span class="sxs-lookup"><span data-stu-id="eee44-114">Service successfully stopped.</span></span>

</dd> <dt>

<span data-ttu-id="eee44-115">**1**</span><span class="sxs-lookup"><span data-stu-id="eee44-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="eee44-116">不支援要求。</span><span class="sxs-lookup"><span data-stu-id="eee44-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eee44-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="eee44-117">Requirements</span></span>



| <span data-ttu-id="eee44-118">需求</span><span class="sxs-lookup"><span data-stu-id="eee44-118">Requirement</span></span> | <span data-ttu-id="eee44-119">值</span><span class="sxs-lookup"><span data-stu-id="eee44-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee44-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eee44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eee44-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eee44-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="eee44-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eee44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eee44-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eee44-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="eee44-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="eee44-124">Namespace</span></span><br/>                | <span data-ttu-id="eee44-125">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eee44-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="eee44-126">標頭</span><span class="sxs-lookup"><span data-stu-id="eee44-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eee44-127"><dt>Sdoias。h</dt></span><span class="sxs-lookup"><span data-stu-id="eee44-127"><dt>Sdoias.h</dt></span></span> </dl>           |
| <span data-ttu-id="eee44-128">MOF</span><span class="sxs-lookup"><span data-stu-id="eee44-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eee44-129"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="eee44-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="eee44-130">DLL</span><span class="sxs-lookup"><span data-stu-id="eee44-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eee44-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eee44-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="eee44-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eee44-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee44-133">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="eee44-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="eee44-134">**Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="eee44-134">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

