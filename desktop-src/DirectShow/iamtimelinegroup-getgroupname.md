---
description: GetGroupName 方法會抓取群組的應用程式定義名稱。
ms.assetid: 402e97d9-abb5-4d8e-8735-1b06d60ab225
title: 'IAMTimelineGroup：： GetGroupName 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 78e3fc736ece3f4a8ebea1c688ce2bc5099f497c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987982"
---
# <a name="iamtimelinegroupgetgroupname-method"></a><span data-ttu-id="59e73-103">IAMTimelineGroup：： GetGroupName 方法</span><span class="sxs-lookup"><span data-stu-id="59e73-103">IAMTimelineGroup::GetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="59e73-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="59e73-104">\[Deprecated.</span></span> <span data-ttu-id="59e73-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="59e73-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="59e73-106">方法會抓取 `GetGroupName` 群組的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="59e73-106">The `GetGroupName` method retrieves the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="59e73-107">語法</span><span class="sxs-lookup"><span data-stu-id="59e73-107">Syntax</span></span>


```C++
HRESULT GetGroupName(
  [out, retval] BSTR *pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="59e73-108">參數</span><span class="sxs-lookup"><span data-stu-id="59e73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59e73-109">*pGroupName* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="59e73-109">*pGroupName* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="59e73-110">接收群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="59e73-110">Receives the name of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59e73-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="59e73-111">Return value</span></span>

<span data-ttu-id="59e73-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="59e73-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59e73-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="59e73-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="59e73-114">備註</span><span class="sxs-lookup"><span data-stu-id="59e73-114">Remarks</span></span>

<span data-ttu-id="59e73-115">方法會配置字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="59e73-115">The method allocates memory for the string.</span></span> <span data-ttu-id="59e73-116">應用程式必須呼叫 **SysFreeString** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="59e73-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="59e73-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="59e73-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="59e73-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="59e73-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="59e73-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="59e73-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59e73-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="59e73-120">Requirements</span></span>



| <span data-ttu-id="59e73-121">需求</span><span class="sxs-lookup"><span data-stu-id="59e73-121">Requirement</span></span> | <span data-ttu-id="59e73-122">值</span><span class="sxs-lookup"><span data-stu-id="59e73-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59e73-123">標頭</span><span class="sxs-lookup"><span data-stu-id="59e73-123">Header</span></span><br/>  | <dl> <span data-ttu-id="59e73-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="59e73-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="59e73-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="59e73-125">Library</span></span><br/> | <dl> <span data-ttu-id="59e73-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="59e73-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59e73-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59e73-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e73-128">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="59e73-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="59e73-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="59e73-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




