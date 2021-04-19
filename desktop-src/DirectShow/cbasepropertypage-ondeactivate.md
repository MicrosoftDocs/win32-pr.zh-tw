---
description: 終結對話方塊視窗時，會呼叫 OnDeactivate 方法。
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: 'CBasePropertyPage. OnDeactivate 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993656"
---
# <a name="cbasepropertypageondeactivate-method"></a><span data-ttu-id="13691-103">CBasePropertyPage. OnDeactivate 方法</span><span class="sxs-lookup"><span data-stu-id="13691-103">CBasePropertyPage.OnDeactivate method</span></span>

<span data-ttu-id="13691-104">`OnDeactivate`當對話方塊視窗終結時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="13691-104">The `OnDeactivate` method is called when the dialog box window is destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="13691-105">語法</span><span class="sxs-lookup"><span data-stu-id="13691-105">Syntax</span></span>


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a><span data-ttu-id="13691-106">參數</span><span class="sxs-lookup"><span data-stu-id="13691-106">Parameters</span></span>

<span data-ttu-id="13691-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="13691-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13691-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="13691-108">Return value</span></span>

<span data-ttu-id="13691-109">基底類別執行會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="13691-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="13691-110">備註</span><span class="sxs-lookup"><span data-stu-id="13691-110">Remarks</span></span>

<span data-ttu-id="13691-111">[**CBasePropertyPage：:D eactivate**](cbasepropertypage-deactivate.md)方法會呼叫 `OnDeactivate` 方法。</span><span class="sxs-lookup"><span data-stu-id="13691-111">The [**CBasePropertyPage::Deactivate**](cbasepropertypage-deactivate.md) method calls the `OnDeactivate` method.</span></span> <span data-ttu-id="13691-112">覆寫 `OnDeactivate` 以釋放衍生類別在 [**CBasePropertyPage：： OnActivate**](cbasepropertypage-onactivate.md) 方法中取得的任何資源，或視需要執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="13691-112">Override `OnDeactivate` to release any resources that the derived class obtained in the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, or to perform other tasks as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="13691-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="13691-113">Requirements</span></span>



| <span data-ttu-id="13691-114">需求</span><span class="sxs-lookup"><span data-stu-id="13691-114">Requirement</span></span> | <span data-ttu-id="13691-115">值</span><span class="sxs-lookup"><span data-stu-id="13691-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13691-116">標頭</span><span class="sxs-lookup"><span data-stu-id="13691-116">Header</span></span><br/>  | <dl> <span data-ttu-id="13691-117"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="13691-117"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="13691-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="13691-118">Library</span></span><br/> | <dl> <span data-ttu-id="13691-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="13691-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13691-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13691-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13691-121">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="13691-121">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




