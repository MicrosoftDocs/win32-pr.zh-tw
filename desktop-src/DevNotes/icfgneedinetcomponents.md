---
description: 判斷在選項中標示的元件是否已安裝在系統上。
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: IcfgNeedInetComponents 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990742"
---
# <a name="icfgneedinetcomponents-function"></a><span data-ttu-id="b0785-103">IcfgNeedInetComponents 函式</span><span class="sxs-lookup"><span data-stu-id="b0785-103">IcfgNeedInetComponents function</span></span>

<span data-ttu-id="b0785-104">判斷在選項中標示的元件是否已安裝在系統上。</span><span class="sxs-lookup"><span data-stu-id="b0785-104">Determines whether components marked in the options are installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0785-105">語法</span><span class="sxs-lookup"><span data-stu-id="b0785-105">Syntax</span></span>


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a><span data-ttu-id="b0785-106">參數</span><span class="sxs-lookup"><span data-stu-id="b0785-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0785-107">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="b0785-107">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="b0785-108">下列旗標的組合，可指定要從下列清單中偵測哪些元件。</span><span class="sxs-lookup"><span data-stu-id="b0785-108">A combination of the following flags that specify which components to detect from the following list.</span></span>



| <span data-ttu-id="b0785-109">值</span><span class="sxs-lookup"><span data-stu-id="b0785-109">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="b0785-110">意義</span><span class="sxs-lookup"><span data-stu-id="b0785-110">Meaning</span></span>                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="b0785-111"><dt>**ICFG \_INSTALLMAIL**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="b0785-111"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="b0785-112">需要交換或網際網路郵件嗎？</span><span class="sxs-lookup"><span data-stu-id="b0785-112">Is Exchange or Internet mail needed?</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="b0785-113"><dt>**ICFG \_INSTALLRAS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b0785-113"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="b0785-114">需要 RAS 嗎？</span><span class="sxs-lookup"><span data-stu-id="b0785-114">Is RAS needed?</span></span><br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="b0785-115"><dt>**ICFG \_INSTALLTCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b0785-115"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="b0785-116">是否需要 TCP/IP？</span><span class="sxs-lookup"><span data-stu-id="b0785-116">Is TCP/IP needed?</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="b0785-117">*lpfNeedComponents*</span><span class="sxs-lookup"><span data-stu-id="b0785-117">*lpfNeedComponents*</span></span> 
</dt> <dd>

<span data-ttu-id="b0785-118">如果這個值不是 **Null**，則如果系統上未安裝一或多個元件，則會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b0785-118">If this value is non-**NULL**, it is **TRUE** on return if one or more components are not installed on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0785-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0785-119">Return value</span></span>

<span data-ttu-id="b0785-120">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b0785-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b0785-121">如果沒有發生錯誤，則會傳回 **錯誤 \_ 成功** 碼。</span><span class="sxs-lookup"><span data-stu-id="b0785-121">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0785-122">備註</span><span class="sxs-lookup"><span data-stu-id="b0785-122">Remarks</span></span>

<span data-ttu-id="b0785-123">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="b0785-123">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0785-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0785-124">Requirements</span></span>



| <span data-ttu-id="b0785-125">需求</span><span class="sxs-lookup"><span data-stu-id="b0785-125">Requirement</span></span> | <span data-ttu-id="b0785-126">值</span><span class="sxs-lookup"><span data-stu-id="b0785-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0785-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b0785-127">DLL</span></span><br/> | <dl> <span data-ttu-id="b0785-128"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0785-128"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
