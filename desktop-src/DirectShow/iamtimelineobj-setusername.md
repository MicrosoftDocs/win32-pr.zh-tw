---
description: SetUserName 方法會設定物件的應用程式定義名稱。
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: 'IAMTimelineObj：： SetUserName 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ec39aece23d38be6fbe2e69f7ded8bc738e04c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001123"
---
# <a name="iamtimelineobjsetusername-method"></a><span data-ttu-id="3ed08-103">IAMTimelineObj：： SetUserName 方法</span><span class="sxs-lookup"><span data-stu-id="3ed08-103">IAMTimelineObj::SetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="3ed08-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3ed08-104">\[Deprecated.</span></span> <span data-ttu-id="3ed08-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3ed08-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3ed08-106">`SetUserName`方法會設定物件的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="3ed08-106">The `SetUserName` method sets an application-defined name for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed08-107">語法</span><span class="sxs-lookup"><span data-stu-id="3ed08-107">Syntax</span></span>


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="3ed08-108">參數</span><span class="sxs-lookup"><span data-stu-id="3ed08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ed08-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="3ed08-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed08-110">包含名稱的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="3ed08-110">Wide-character string that contains the name.</span></span> <span data-ttu-id="3ed08-111">長度超過256個字元的字串可能會被截斷。</span><span class="sxs-lookup"><span data-stu-id="3ed08-111">Strings longer than 256 characters might be truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ed08-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ed08-112">Return value</span></span>

<span data-ttu-id="3ed08-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3ed08-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ed08-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3ed08-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ed08-115">備註</span><span class="sxs-lookup"><span data-stu-id="3ed08-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3ed08-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="3ed08-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3ed08-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3ed08-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3ed08-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="3ed08-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3ed08-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ed08-119">Requirements</span></span>



| <span data-ttu-id="3ed08-120">需求</span><span class="sxs-lookup"><span data-stu-id="3ed08-120">Requirement</span></span> | <span data-ttu-id="3ed08-121">值</span><span class="sxs-lookup"><span data-stu-id="3ed08-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed08-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3ed08-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3ed08-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ed08-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3ed08-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ed08-124">Library</span></span><br/> | <dl> <span data-ttu-id="3ed08-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ed08-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ed08-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ed08-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed08-127">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="3ed08-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="3ed08-128">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="3ed08-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




