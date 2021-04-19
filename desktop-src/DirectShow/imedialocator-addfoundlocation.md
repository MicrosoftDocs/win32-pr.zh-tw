---
description: AddFoundLocation 方法會將目錄新增至目錄快取。
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: 'IMediaLocator：： AddFoundLocation 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76d878e5b013b8c6a061d777d4ec837bca85f8e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990036"
---
# <a name="imedialocatoraddfoundlocation-method"></a><span data-ttu-id="0a822-103">IMediaLocator：： AddFoundLocation 方法</span><span class="sxs-lookup"><span data-stu-id="0a822-103">IMediaLocator::AddFoundLocation method</span></span>

> [!Note]  
> <span data-ttu-id="0a822-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="0a822-104">\[Deprecated.</span></span> <span data-ttu-id="0a822-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="0a822-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a822-106">`AddFoundLocation`方法會將目錄新增至目錄快取。</span><span class="sxs-lookup"><span data-stu-id="0a822-106">The `AddFoundLocation` method adds a directory to the directory cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a822-107">語法</span><span class="sxs-lookup"><span data-stu-id="0a822-107">Syntax</span></span>


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a><span data-ttu-id="0a822-108">參數</span><span class="sxs-lookup"><span data-stu-id="0a822-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a822-109">*DirectoryName*</span><span class="sxs-lookup"><span data-stu-id="0a822-109">*DirectoryName*</span></span> 
</dt> <dd>

<span data-ttu-id="0a822-110">要新增至快取的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="0a822-110">Directory path to add to the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a822-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a822-111">Return value</span></span>

<span data-ttu-id="0a822-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0a822-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a822-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0a822-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a822-114">備註</span><span class="sxs-lookup"><span data-stu-id="0a822-114">Remarks</span></span>

<span data-ttu-id="0a822-115">媒體定位器會保存目錄路徑的快取，其中已在過去搜尋中成功找到檔案。</span><span class="sxs-lookup"><span data-stu-id="0a822-115">The media locator keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="0a822-116">當它成功找到檔案時，它會將目錄新增至快取。</span><span class="sxs-lookup"><span data-stu-id="0a822-116">When it successfully locates a file, it adds the directory to the cache.</span></span>

> [!Note]  
> <span data-ttu-id="0a822-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="0a822-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0a822-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0a822-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0a822-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="0a822-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a822-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a822-120">Requirements</span></span>



| <span data-ttu-id="0a822-121">需求</span><span class="sxs-lookup"><span data-stu-id="0a822-121">Requirement</span></span> | <span data-ttu-id="0a822-122">值</span><span class="sxs-lookup"><span data-stu-id="0a822-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a822-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0a822-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0a822-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a822-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0a822-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a822-125">Library</span></span><br/> | <dl> <span data-ttu-id="0a822-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a822-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a822-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a822-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a822-128">**IMediaLocator 介面**</span><span class="sxs-lookup"><span data-stu-id="0a822-128">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="0a822-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="0a822-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




