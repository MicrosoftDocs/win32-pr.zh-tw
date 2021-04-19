---
description: 關閉 [OC 管理員]。
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: OcTerminate 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987042"
---
# <a name="octerminate-function"></a><span data-ttu-id="f246b-103">OcTerminate 函式</span><span class="sxs-lookup"><span data-stu-id="f246b-103">OcTerminate function</span></span>

<span data-ttu-id="f246b-104">關閉 [OC 管理員]。</span><span class="sxs-lookup"><span data-stu-id="f246b-104">Closes the OC manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="f246b-105">語法</span><span class="sxs-lookup"><span data-stu-id="f246b-105">Syntax</span></span>


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a><span data-ttu-id="f246b-106">參數</span><span class="sxs-lookup"><span data-stu-id="f246b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f246b-107">*OcManagerCoNtext* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f246b-107">*OcManagerContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f246b-108">在輸入時，包含 [**OcInitialize**](ocinitialize.md)所傳回的 OC 管理員內容指標。</span><span class="sxs-lookup"><span data-stu-id="f246b-108">On input, contains the OC manager context pointer returned by [**OcInitialize**](ocinitialize.md).</span></span> <span data-ttu-id="f246b-109">在輸出時，接收 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f246b-109">On output, receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f246b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f246b-110">Return value</span></span>

<span data-ttu-id="f246b-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f246b-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f246b-112">備註</span><span class="sxs-lookup"><span data-stu-id="f246b-112">Remarks</span></span>

<span data-ttu-id="f246b-113">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="f246b-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f246b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f246b-114">Requirements</span></span>



| <span data-ttu-id="f246b-115">需求</span><span class="sxs-lookup"><span data-stu-id="f246b-115">Requirement</span></span> | <span data-ttu-id="f246b-116">值</span><span class="sxs-lookup"><span data-stu-id="f246b-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f246b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="f246b-117">DLL</span></span><br/> | <dl> <span data-ttu-id="f246b-118"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f246b-118"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f246b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f246b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f246b-120">**OcInitialize**</span><span class="sxs-lookup"><span data-stu-id="f246b-120">**OcInitialize**</span></span>](ocinitialize.md)
</dt> </dl>

 

 
