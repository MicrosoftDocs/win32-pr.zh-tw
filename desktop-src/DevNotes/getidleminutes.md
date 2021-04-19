---
description: 取得使用者的最後一個活動之後的時間長度（以分鐘為單位）。
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: GetIdleMinutes 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: da3064ea96eb8e9835ed1e9d2f564bf922d2f091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978663"
---
# <a name="getidleminutes-function"></a><span data-ttu-id="6aa86-103">GetIdleMinutes 函式</span><span class="sxs-lookup"><span data-stu-id="6aa86-103">GetIdleMinutes function</span></span>

<span data-ttu-id="6aa86-104">\[這項功能不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="6aa86-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="6aa86-105">請改用 **GetLastInputInfo** 函數。\]</span><span class="sxs-lookup"><span data-stu-id="6aa86-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="6aa86-106">取得使用者的最後一個活動之後的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="6aa86-106">Gets the length of time, in minutes, since the user's last activity.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa86-107">語法</span><span class="sxs-lookup"><span data-stu-id="6aa86-107">Syntax</span></span>


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="6aa86-108">參數</span><span class="sxs-lookup"><span data-stu-id="6aa86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aa86-109">*>dwreserved*</span><span class="sxs-lookup"><span data-stu-id="6aa86-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="6aa86-110">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="6aa86-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aa86-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6aa86-111">Return value</span></span>

<span data-ttu-id="6aa86-112">傳回使用者的最後一個活動之後的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="6aa86-112">Returns the number of minutes since the user's last activity.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aa86-113">備註</span><span class="sxs-lookup"><span data-stu-id="6aa86-113">Remarks</span></span>

<span data-ttu-id="6aa86-114">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="6aa86-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="6aa86-115">此函式不是依名稱匯出;呼叫 **GetProcAddress** 時指定序數8。</span><span class="sxs-lookup"><span data-stu-id="6aa86-115">This function is not exported by name; specify ordinal 8 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aa86-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6aa86-116">Requirements</span></span>



| <span data-ttu-id="6aa86-117">需求</span><span class="sxs-lookup"><span data-stu-id="6aa86-117">Requirement</span></span> | <span data-ttu-id="6aa86-118">值</span><span class="sxs-lookup"><span data-stu-id="6aa86-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa86-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6aa86-119">DLL</span></span><br/> | <dl> <span data-ttu-id="6aa86-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aa86-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6aa86-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6aa86-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa86-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="6aa86-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
