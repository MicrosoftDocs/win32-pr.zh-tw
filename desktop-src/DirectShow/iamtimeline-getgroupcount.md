---
description: GetGroupCount 方法會抓取時間軸中包含的群組數目。
ms.assetid: 24351e03-3132-4363-8171-eae517fb770a
title: 'IAMTimeline：： GetGroupCount 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroupCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4d16cf44839b05f39bc747cb89eda77842caa04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990737"
---
# <a name="iamtimelinegetgroupcount-method"></a><span data-ttu-id="d9f20-103">IAMTimeline：： GetGroupCount 方法</span><span class="sxs-lookup"><span data-stu-id="d9f20-103">IAMTimeline::GetGroupCount method</span></span>

> [!Note]  
> <span data-ttu-id="d9f20-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d9f20-104">\[Deprecated.</span></span> <span data-ttu-id="d9f20-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d9f20-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d9f20-106">`GetGroupCount`方法會抓取時間軸中包含的群組數目。</span><span class="sxs-lookup"><span data-stu-id="d9f20-106">The `GetGroupCount` method retrieves the number of groups that are contained in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f20-107">語法</span><span class="sxs-lookup"><span data-stu-id="d9f20-107">Syntax</span></span>


```C++
HRESULT GetGroupCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="d9f20-108">參數</span><span class="sxs-lookup"><span data-stu-id="d9f20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9f20-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="d9f20-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="d9f20-110">接收時間軸中的群組數目。</span><span class="sxs-lookup"><span data-stu-id="d9f20-110">Receives the number of groups in the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9f20-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9f20-111">Return value</span></span>

<span data-ttu-id="d9f20-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d9f20-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9f20-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d9f20-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f20-114">備註</span><span class="sxs-lookup"><span data-stu-id="d9f20-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d9f20-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d9f20-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d9f20-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d9f20-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d9f20-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d9f20-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d9f20-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9f20-118">Requirements</span></span>



| <span data-ttu-id="d9f20-119">需求</span><span class="sxs-lookup"><span data-stu-id="d9f20-119">Requirement</span></span> | <span data-ttu-id="d9f20-120">值</span><span class="sxs-lookup"><span data-stu-id="d9f20-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f20-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d9f20-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d9f20-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9f20-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d9f20-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="d9f20-123">Library</span></span><br/> | <dl> <span data-ttu-id="d9f20-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9f20-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f20-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9f20-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f20-126">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="d9f20-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="d9f20-127">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="d9f20-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




