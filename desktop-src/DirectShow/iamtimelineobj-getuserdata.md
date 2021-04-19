---
description: GetUserData 方法會抓取應用程式定義的持續性資料。
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'IAMTimelineObj：： GetUserData 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9dda74980dcdae9cd73e749d9cb4324b4c6357f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995432"
---
# <a name="iamtimelineobjgetuserdata-method"></a><span data-ttu-id="8ac48-103">IAMTimelineObj：： GetUserData 方法</span><span class="sxs-lookup"><span data-stu-id="8ac48-103">IAMTimelineObj::GetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="8ac48-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="8ac48-104">\[Deprecated.</span></span> <span data-ttu-id="8ac48-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="8ac48-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8ac48-106">方法會抓取 `GetUserData` 應用程式定義的持續性資料。</span><span class="sxs-lookup"><span data-stu-id="8ac48-106">The `GetUserData` method retrieves the application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ac48-107">語法</span><span class="sxs-lookup"><span data-stu-id="8ac48-107">Syntax</span></span>


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="8ac48-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ac48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ac48-109">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="8ac48-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac48-110">接收資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="8ac48-110">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="8ac48-111">若要判斷要配置的緩衝區大小，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8ac48-111">To determine the size of buffer to allocate, set this parameter to **NULL**.</span></span> <span data-ttu-id="8ac48-112">所需的大小會在 *pSize* 中傳回。</span><span class="sxs-lookup"><span data-stu-id="8ac48-112">The required size is returned in *pSize*.</span></span>

</dd> <dt>

<span data-ttu-id="8ac48-113">*pSize*</span><span class="sxs-lookup"><span data-stu-id="8ac48-113">*pSize*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac48-114">接收資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8ac48-114">Receives the size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ac48-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ac48-115">Return value</span></span>

<span data-ttu-id="8ac48-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8ac48-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ac48-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8ac48-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ac48-118">備註</span><span class="sxs-lookup"><span data-stu-id="8ac48-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ac48-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="8ac48-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8ac48-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="8ac48-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8ac48-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="8ac48-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ac48-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ac48-122">Requirements</span></span>



| <span data-ttu-id="8ac48-123">需求</span><span class="sxs-lookup"><span data-stu-id="8ac48-123">Requirement</span></span> | <span data-ttu-id="8ac48-124">值</span><span class="sxs-lookup"><span data-stu-id="8ac48-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac48-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8ac48-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8ac48-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ac48-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8ac48-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ac48-127">Library</span></span><br/> | <dl> <span data-ttu-id="8ac48-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ac48-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ac48-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ac48-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac48-130">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="8ac48-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="8ac48-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="8ac48-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




