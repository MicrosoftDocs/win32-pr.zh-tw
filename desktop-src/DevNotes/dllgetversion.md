---
description: DllGetVersion 函數會使用 CABINETDLLVERSIONINFO 結構來抓取 Cabinet.dll 的版本號碼。
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: DllGetVersion 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994237"
---
# <a name="dllgetversion-function"></a><span data-ttu-id="017a0-103">DllGetVersion 函式</span><span class="sxs-lookup"><span data-stu-id="017a0-103">DllGetVersion function</span></span>

<span data-ttu-id="017a0-104">\[不再支援此函式，因此無法保證其行為。\]</span><span class="sxs-lookup"><span data-stu-id="017a0-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="017a0-105">**DllGetVersion** 函數會使用 [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md)結構來抓取 Cabinet.dll 的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="017a0-105">The **DllGetVersion** function retrieves the version number of Cabinet.dll using the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="017a0-106">語法</span><span class="sxs-lookup"><span data-stu-id="017a0-106">Syntax</span></span>


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a><span data-ttu-id="017a0-107">參數</span><span class="sxs-lookup"><span data-stu-id="017a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="017a0-108">*pcdvi*</span><span class="sxs-lookup"><span data-stu-id="017a0-108">*pcdvi*</span></span> 
</dt> <dd>

<span data-ttu-id="017a0-109">包含版本資訊之 [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="017a0-109">Pointer to the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure that contains the version information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="017a0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="017a0-110">Return value</span></span>

<span data-ttu-id="017a0-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="017a0-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="017a0-112">備註</span><span class="sxs-lookup"><span data-stu-id="017a0-112">Remarks</span></span>

<span data-ttu-id="017a0-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="017a0-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="017a0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="017a0-114">Requirements</span></span>



| <span data-ttu-id="017a0-115">需求</span><span class="sxs-lookup"><span data-stu-id="017a0-115">Requirement</span></span> | <span data-ttu-id="017a0-116">值</span><span class="sxs-lookup"><span data-stu-id="017a0-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="017a0-117">DLL</span><span class="sxs-lookup"><span data-stu-id="017a0-117">DLL</span></span><br/> | <dl> <span data-ttu-id="017a0-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="017a0-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="017a0-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="017a0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017a0-120">**CABINETDLLVERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="017a0-120">**CABINETDLLVERSIONINFO**</span></span>](cabinetdllversioninfo.md)
</dt> <dt>

[<span data-ttu-id="017a0-121">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="017a0-121">**GetDllVersion**</span></span>](getdllversion.md)
</dt> </dl>

 

 
