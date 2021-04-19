---
title: IWMPLibraryServices getLibraryByType 方法
description: GetLibraryByType 方法會傳回 IWMPLibrary 介面，代表具有指定之類型和索引的程式庫。
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- getLibraryByType 方法 Windows Media Player
- getLibraryByType 方法 Windows Media Player，IWMPLibraryServices 介面
- IWMPLibraryServices 介面 Windows Media Player，getLibraryByType 方法
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994861"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a><span data-ttu-id="b8e2d-106">IWMPLibraryServices：： getLibraryByType 方法</span><span class="sxs-lookup"><span data-stu-id="b8e2d-106">IWMPLibraryServices::getLibraryByType method</span></span>

<span data-ttu-id="b8e2d-107">**GetLibraryByType** 方法會傳回 **IWMPLibrary** 介面，代表具有指定之類型和索引的程式庫。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-107">The **getLibraryByType** method returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e2d-108">語法</span><span class="sxs-lookup"><span data-stu-id="b8e2d-108">Syntax</span></span>


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a><span data-ttu-id="b8e2d-109">參數</span><span class="sxs-lookup"><span data-stu-id="b8e2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e2d-110">*wmplt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8e2d-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e2d-111">**WMPLib. WMPLibraryType** 列舉中的值，這個值會指定要取出的程式庫類型。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b8e2d-112">*lIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8e2d-112">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e2d-113">要抓取之程式庫索引的 **system.object。**</span><span class="sxs-lookup"><span data-stu-id="b8e2d-113">A **System.Int32** that is the index of the library to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e2d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8e2d-114">Return value</span></span>

<span data-ttu-id="b8e2d-115">傳回之程式庫的 **WMPLib IWMPLibrary** 介面。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-115">A **WMPLib.IWMPLibrary** interface for the library that is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8e2d-116">備註</span><span class="sxs-lookup"><span data-stu-id="b8e2d-116">Remarks</span></span>

<span data-ttu-id="b8e2d-117">只有一個本機程式庫，而只有包含媒體內容的資料 Cd 和 Dvd 上才能使用光碟櫃。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-117">There is only one local library, and disc libraries are available only on data CDs and DVDs that contain media content.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e2d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8e2d-118">Requirements</span></span>



| <span data-ttu-id="b8e2d-119">需求</span><span class="sxs-lookup"><span data-stu-id="b8e2d-119">Requirement</span></span> | <span data-ttu-id="b8e2d-120">值</span><span class="sxs-lookup"><span data-stu-id="b8e2d-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e2d-121">版本</span><span class="sxs-lookup"><span data-stu-id="b8e2d-121">Version</span></span><br/>   | <span data-ttu-id="b8e2d-122">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="b8e2d-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="b8e2d-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8e2d-123">Namespace</span></span><br/> | <span data-ttu-id="b8e2d-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b8e2d-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b8e2d-125">組件</span><span class="sxs-lookup"><span data-stu-id="b8e2d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b8e2d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b8e2d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e2d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8e2d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e2d-128">**IWMPLibrary 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8e2d-128">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8e2d-129">**IWMPLibraryServices 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8e2d-129">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8e2d-130">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="b8e2d-130">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





