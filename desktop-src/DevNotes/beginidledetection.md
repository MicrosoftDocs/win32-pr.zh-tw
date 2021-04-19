---
description: 開始監視非活動狀態。
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: BeginIdleDetection 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993418"
---
# <a name="beginidledetection-function"></a><span data-ttu-id="30e18-103">BeginIdleDetection 函式</span><span class="sxs-lookup"><span data-stu-id="30e18-103">BeginIdleDetection function</span></span>

<span data-ttu-id="30e18-104">\[這項功能不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="30e18-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="30e18-105">請改用 **GetLastInputInfo** 函數。\]</span><span class="sxs-lookup"><span data-stu-id="30e18-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="30e18-106">開始監視非活動狀態。</span><span class="sxs-lookup"><span data-stu-id="30e18-106">Begins monitoring inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="30e18-107">語法</span><span class="sxs-lookup"><span data-stu-id="30e18-107">Syntax</span></span>


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="30e18-108">參數</span><span class="sxs-lookup"><span data-stu-id="30e18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e18-109">*pfnCallback*</span><span class="sxs-lookup"><span data-stu-id="30e18-109">*pfnCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="30e18-110">當閒置狀態變更時所呼叫的函數。</span><span class="sxs-lookup"><span data-stu-id="30e18-110">The function that is called when the idle state changes.</span></span> <span data-ttu-id="30e18-111">此回呼的定義如下：</span><span class="sxs-lookup"><span data-stu-id="30e18-111">This callback is defined as follows:</span></span>

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

<span data-ttu-id="30e18-112">*dwIdleMin*</span><span class="sxs-lookup"><span data-stu-id="30e18-112">*dwIdleMin*</span></span> 
</dt> <dd>

<span data-ttu-id="30e18-113">對回呼函式進行呼叫之前的非活動分鐘數。</span><span class="sxs-lookup"><span data-stu-id="30e18-113">The number of minutes of inactivity before the call is made to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="30e18-114">*>dwreserved*</span><span class="sxs-lookup"><span data-stu-id="30e18-114">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="30e18-115">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="30e18-115">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e18-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="30e18-116">Return value</span></span>

<span data-ttu-id="30e18-117">如果函式成功，則傳回 0;否則，它會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="30e18-117">Returns 0 if the function succeeds; otherwise, it returns an error code.</span></span> <span data-ttu-id="30e18-118">例如，如果 *>dwreserved* 是0以外的任何一項，則會傳回 **錯誤的 \_ \_ 資料無效** 。</span><span class="sxs-lookup"><span data-stu-id="30e18-118">For example, if *dwReserved* is anything other than 0, **ERROR\_INVALID\_DATA** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="30e18-119">備註</span><span class="sxs-lookup"><span data-stu-id="30e18-119">Remarks</span></span>

<span data-ttu-id="30e18-120">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="30e18-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="30e18-121">此函式不是依名稱匯出;呼叫 **GetProcAddress** 時指定序數3。</span><span class="sxs-lookup"><span data-stu-id="30e18-121">This function is not exported by name; specify ordinal 3 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="30e18-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="30e18-122">Requirements</span></span>



| <span data-ttu-id="30e18-123">需求</span><span class="sxs-lookup"><span data-stu-id="30e18-123">Requirement</span></span> | <span data-ttu-id="30e18-124">值</span><span class="sxs-lookup"><span data-stu-id="30e18-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30e18-125">DLL</span><span class="sxs-lookup"><span data-stu-id="30e18-125">DLL</span></span><br/> | <dl> <span data-ttu-id="30e18-126"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30e18-126"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30e18-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30e18-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e18-128">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="30e18-128">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
