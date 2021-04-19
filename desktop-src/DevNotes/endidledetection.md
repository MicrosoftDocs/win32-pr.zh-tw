---
description: 結束非活動狀態的監視。
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: EndIdleDetection 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978726"
---
# <a name="endidledetection-function"></a><span data-ttu-id="95511-103">EndIdleDetection 函式</span><span class="sxs-lookup"><span data-stu-id="95511-103">EndIdleDetection function</span></span>

<span data-ttu-id="95511-104">\[這項功能不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="95511-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="95511-105">請改用 **GetLastInputInfo** 函數。\]</span><span class="sxs-lookup"><span data-stu-id="95511-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="95511-106">結束非活動狀態的監視。</span><span class="sxs-lookup"><span data-stu-id="95511-106">Ends monitoring of inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="95511-107">語法</span><span class="sxs-lookup"><span data-stu-id="95511-107">Syntax</span></span>


```C++
BOOL WINAPI EndIdleDetection(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="95511-108">參數</span><span class="sxs-lookup"><span data-stu-id="95511-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95511-109">*>dwreserved*</span><span class="sxs-lookup"><span data-stu-id="95511-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="95511-110">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="95511-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95511-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95511-111">Return value</span></span>

<span data-ttu-id="95511-112">如果函式成功，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="95511-112">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="95511-113">備註</span><span class="sxs-lookup"><span data-stu-id="95511-113">Remarks</span></span>

<span data-ttu-id="95511-114">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="95511-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="95511-115">此函式不是依名稱匯出;呼叫 **GetProcAddress** 時指定序數4。</span><span class="sxs-lookup"><span data-stu-id="95511-115">This function is not exported by name; specify ordinal 4 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="95511-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="95511-116">Requirements</span></span>



| <span data-ttu-id="95511-117">需求</span><span class="sxs-lookup"><span data-stu-id="95511-117">Requirement</span></span> | <span data-ttu-id="95511-118">值</span><span class="sxs-lookup"><span data-stu-id="95511-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95511-119">DLL</span><span class="sxs-lookup"><span data-stu-id="95511-119">DLL</span></span><br/> | <dl> <span data-ttu-id="95511-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95511-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95511-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95511-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95511-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="95511-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
