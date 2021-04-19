---
title: IWMPLibraryServices getCountByType 方法
description: GetCountByType 方法會傳回指定類型的可用程式庫計數。
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- getCountByType 方法 Windows Media Player
- getCountByType 方法 Windows Media Player，IWMPLibraryServices 介面
- IWMPLibraryServices 介面 Windows Media Player，getCountByType 方法
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978482"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a><span data-ttu-id="1d64e-106">IWMPLibraryServices：： getCountByType 方法</span><span class="sxs-lookup"><span data-stu-id="1d64e-106">IWMPLibraryServices::getCountByType method</span></span>

<span data-ttu-id="1d64e-107">**GetCountByType** 方法會傳回指定類型的可用程式庫計數。</span><span class="sxs-lookup"><span data-stu-id="1d64e-107">The **getCountByType** method returns the count of available libraries of a specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d64e-108">語法</span><span class="sxs-lookup"><span data-stu-id="1d64e-108">Syntax</span></span>


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a><span data-ttu-id="1d64e-109">參數</span><span class="sxs-lookup"><span data-stu-id="1d64e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d64e-110">*wmplt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d64e-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d64e-111">**WMPLib. WMPLibraryType** 列舉中的值，這個值會指定要計算的程式庫類型。</span><span class="sxs-lookup"><span data-stu-id="1d64e-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d64e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d64e-112">Return value</span></span>

<span data-ttu-id="1d64e-113">為程式庫計數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="1d64e-113">A **System.Int32** that is the library count.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d64e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d64e-114">Requirements</span></span>



| <span data-ttu-id="1d64e-115">需求</span><span class="sxs-lookup"><span data-stu-id="1d64e-115">Requirement</span></span> | <span data-ttu-id="1d64e-116">值</span><span class="sxs-lookup"><span data-stu-id="1d64e-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d64e-117">版本</span><span class="sxs-lookup"><span data-stu-id="1d64e-117">Version</span></span><br/>   | <span data-ttu-id="1d64e-118">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="1d64e-118">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="1d64e-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d64e-119">Namespace</span></span><br/> | <span data-ttu-id="1d64e-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1d64e-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1d64e-121">組件</span><span class="sxs-lookup"><span data-stu-id="1d64e-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1d64e-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="1d64e-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d64e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d64e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d64e-124">**IWMPLibraryServices 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1d64e-124">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d64e-125">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="1d64e-125">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





