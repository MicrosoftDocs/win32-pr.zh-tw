---
description: SetGroupName 方法會設定群組的應用程式定義名稱。
ms.assetid: e1d8a91b-d5b9-42a4-9b98-582e1a57ac51
title: 'IAMTimelineGroup：： SetGroupName 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 327bf0384ce484353ac41c069ddf580c674b0b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982540"
---
# <a name="iamtimelinegroupsetgroupname-method"></a><span data-ttu-id="ce709-103">IAMTimelineGroup：： SetGroupName 方法</span><span class="sxs-lookup"><span data-stu-id="ce709-103">IAMTimelineGroup::SetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="ce709-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ce709-104">\[Deprecated.</span></span> <span data-ttu-id="ce709-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ce709-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ce709-106">`SetGroupName`方法會設定群組的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="ce709-106">The `SetGroupName` method sets the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce709-107">語法</span><span class="sxs-lookup"><span data-stu-id="ce709-107">Syntax</span></span>


```C++
HRESULT SetGroupName(
   BSTR pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="ce709-108">參數</span><span class="sxs-lookup"><span data-stu-id="ce709-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce709-109">*pGroupName*</span><span class="sxs-lookup"><span data-stu-id="ce709-109">*pGroupName*</span></span> 
</dt> <dd>

<span data-ttu-id="ce709-110">指定群組名稱的 **BSTR** 。</span><span class="sxs-lookup"><span data-stu-id="ce709-110">**BSTR** that specifies the name of the group.</span></span> <span data-ttu-id="ce709-111">名稱的長度上限為256個字元，包括 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="ce709-111">The maximum length of the name is 256 characters, incuding the null terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce709-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce709-112">Return value</span></span>

<span data-ttu-id="ce709-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ce709-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce709-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ce709-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce709-115">備註</span><span class="sxs-lookup"><span data-stu-id="ce709-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce709-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ce709-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ce709-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ce709-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ce709-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ce709-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce709-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce709-119">Requirements</span></span>



| <span data-ttu-id="ce709-120">需求</span><span class="sxs-lookup"><span data-stu-id="ce709-120">Requirement</span></span> | <span data-ttu-id="ce709-121">值</span><span class="sxs-lookup"><span data-stu-id="ce709-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce709-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ce709-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ce709-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce709-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ce709-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce709-124">Library</span></span><br/> | <dl> <span data-ttu-id="ce709-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce709-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce709-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce709-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce709-127">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="ce709-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="ce709-128">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="ce709-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




