---
description: 取得目前正在執行之作業系統的版本資訊。
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: 'RtlGetVersion 函式 (Ntddk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110437"
---
# <a name="rtlgetversion-function"></a><span data-ttu-id="93a1c-103">RtlGetVersion 函式</span><span class="sxs-lookup"><span data-stu-id="93a1c-103">RtlGetVersion function</span></span>

<span data-ttu-id="93a1c-104">取得目前正在執行之作業系統的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="93a1c-104">Gets version information about the currently running operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="93a1c-105">語法</span><span class="sxs-lookup"><span data-stu-id="93a1c-105">Syntax</span></span>


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a><span data-ttu-id="93a1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="93a1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93a1c-107">*lpVersionInformation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93a1c-107">*lpVersionInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93a1c-108">[**Rtl \_ OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow)結構或 [**rtl \_ OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw)結構的指標，其中包含目前執行之作業系統的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="93a1c-108">Pointer to either a [**RTL\_OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) structure or a [**RTL\_OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) structure that contains the version information about the currently running operating system.</span></span> <span data-ttu-id="93a1c-109">呼叫端會將結構的 **dwOSVersionInfoSize** 成員設定為所使用之結構的大小（以位元組為單位），以指定要使用哪一個輸入結構。</span><span class="sxs-lookup"><span data-stu-id="93a1c-109">A caller specifies which input structure is used by setting the **dwOSVersionInfoSize** member of the structure to the size in bytes of the structure that is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93a1c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="93a1c-110">Return value</span></span>

<span data-ttu-id="93a1c-111">傳回狀態 \_ 成功。</span><span class="sxs-lookup"><span data-stu-id="93a1c-111">Returns STATUS\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="93a1c-112">備註</span><span class="sxs-lookup"><span data-stu-id="93a1c-112">Remarks</span></span>

<span data-ttu-id="93a1c-113">**RtlGetVersion** 等同于 Windows SDK 中的 [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="93a1c-113">**RtlGetVersion** is the equivalent of the [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function in the Windows SDK.</span></span> <span data-ttu-id="93a1c-114">請參閱 Windows SDK 中的範例，其中顯示如何取得系統版本。</span><span class="sxs-lookup"><span data-stu-id="93a1c-114">See the example in the Windows SDK that shows how to get the system version.</span></span>

<span data-ttu-id="93a1c-115">使用 **RtlGetVersion** 來判斷特定版本的作業系統是否正在執行時，呼叫端應該檢查是否有大於或等於所需版本號碼的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="93a1c-115">When using **RtlGetVersion** to determine whether a particular version of the operating system is running, a caller should check for version numbers that are greater than or equal to the required version number.</span></span> <span data-ttu-id="93a1c-116">這可確保版本測試可在較新的 Windows 版本中成功執行。</span><span class="sxs-lookup"><span data-stu-id="93a1c-116">This ensures that a version test succeeds for later versions of Windows.</span></span>

<span data-ttu-id="93a1c-117">因為可以在可轉散發 DLL 中新增作業系統功能，所以只檢查主要和次要版本號碼，並不是確認特定系統功能是否存在的最可靠方式。</span><span class="sxs-lookup"><span data-stu-id="93a1c-117">Because operating system features can be added in a redistributable DLL, checking only the major and minor version numbers is not the most reliable way to verify the presence of a specific system feature.</span></span> <span data-ttu-id="93a1c-118">驅動程式應該使用 [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) 來測試特定系統功能是否存在。</span><span class="sxs-lookup"><span data-stu-id="93a1c-118">A driver should use [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) to test for the presence of a specific system feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="93a1c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="93a1c-119">Requirements</span></span>



| <span data-ttu-id="93a1c-120">需求</span><span class="sxs-lookup"><span data-stu-id="93a1c-120">Requirement</span></span> | <span data-ttu-id="93a1c-121">值</span><span class="sxs-lookup"><span data-stu-id="93a1c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a1c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93a1c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="93a1c-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93a1c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="93a1c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93a1c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="93a1c-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93a1c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="93a1c-126">目標平台</span><span class="sxs-lookup"><span data-stu-id="93a1c-126">Target platform</span></span><br/>          | <dl> <span data-ttu-id="93a1c-127"><dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="93a1c-127"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl>                  |
| <span data-ttu-id="93a1c-128">標頭</span><span class="sxs-lookup"><span data-stu-id="93a1c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="93a1c-129"><dt>Ntddk (包含 Ntddk) </dt></span><span class="sxs-lookup"><span data-stu-id="93a1c-129"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                                     |
| <span data-ttu-id="93a1c-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="93a1c-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="93a1c-131"><dt>Ntdll.dll .lib;</dt><dt>Ntoskrnl.exe .lib</dt></span><span class="sxs-lookup"><span data-stu-id="93a1c-131"><dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="93a1c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="93a1c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93a1c-133"><dt>Ntdll.dll;</dt><dt>NtosKrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93a1c-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93a1c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93a1c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a1c-135">**PsGetVersion**</span><span class="sxs-lookup"><span data-stu-id="93a1c-135">**PsGetVersion**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
