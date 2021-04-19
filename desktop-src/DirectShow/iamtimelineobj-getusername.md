---
description: GetUserName 方法會抓取物件的應用程式定義名稱。
ms.assetid: 7d172ec5-9cb7-4418-a628-a109944077a6
title: 'IAMTimelineObj：： GetUserName 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: efca014493cb5631e058927256bd1586aaca7ab7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990936"
---
# <a name="iamtimelineobjgetusername-method"></a><span data-ttu-id="e7874-103">IAMTimelineObj：： GetUserName 方法</span><span class="sxs-lookup"><span data-stu-id="e7874-103">IAMTimelineObj::GetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="e7874-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="e7874-104">\[Deprecated.</span></span> <span data-ttu-id="e7874-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="e7874-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e7874-106">方法會抓取 `GetUserName` 物件的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="e7874-106">The `GetUserName` method retrieves the object's application-defined name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7874-107">語法</span><span class="sxs-lookup"><span data-stu-id="e7874-107">Syntax</span></span>


```C++
HRESULT GetUserName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e7874-108">參數</span><span class="sxs-lookup"><span data-stu-id="e7874-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7874-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="e7874-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e7874-110">以 **BSTR** 的形式接收物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7874-110">Receives the name of the object as a **BSTR**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7874-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7874-111">Return value</span></span>

<span data-ttu-id="e7874-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e7874-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7874-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e7874-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7874-114">備註</span><span class="sxs-lookup"><span data-stu-id="e7874-114">Remarks</span></span>

<span data-ttu-id="e7874-115">方法會配置字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e7874-115">The method allocates memory for the string.</span></span> <span data-ttu-id="e7874-116">應用程式必須呼叫 **SysFreeString** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="e7874-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="e7874-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="e7874-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7874-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e7874-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e7874-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="e7874-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7874-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7874-120">Requirements</span></span>



| <span data-ttu-id="e7874-121">需求</span><span class="sxs-lookup"><span data-stu-id="e7874-121">Requirement</span></span> | <span data-ttu-id="e7874-122">值</span><span class="sxs-lookup"><span data-stu-id="e7874-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7874-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e7874-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e7874-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7874-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e7874-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="e7874-125">Library</span></span><br/> | <dl> <span data-ttu-id="e7874-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7874-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7874-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7874-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7874-128">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="e7874-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e7874-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="e7874-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




