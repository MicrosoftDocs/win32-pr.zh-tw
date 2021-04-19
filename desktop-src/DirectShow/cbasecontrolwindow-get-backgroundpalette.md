---
description: Get \_ BackgroundPalette 方法會抓取背景旗標中的已實現調色板。
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: 'CBaseControlWindow.get_BackgroundPalette 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997638"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a><span data-ttu-id="fb401-103">CBaseControlWindow. 取得 \_ BackgroundPalette 方法</span><span class="sxs-lookup"><span data-stu-id="fb401-103">CBaseControlWindow.get\_BackgroundPalette method</span></span>

<span data-ttu-id="fb401-104">方法會抓取 `get_BackgroundPalette` 背景旗標中的已實現調色板。</span><span class="sxs-lookup"><span data-stu-id="fb401-104">The `get_BackgroundPalette` method retrieves the realized palette in the background flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb401-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb401-105">Syntax</span></span>


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="fb401-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb401-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb401-107">*pBackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="fb401-107">*pBackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="fb401-108">自動化布林值旗標的指標 (0 是 off，1是) 。</span><span class="sxs-lookup"><span data-stu-id="fb401-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb401-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb401-109">Return value</span></span>

<span data-ttu-id="fb401-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="fb401-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb401-111">備註</span><span class="sxs-lookup"><span data-stu-id="fb401-111">Remarks</span></span>

<span data-ttu-id="fb401-112">此成員函式會實 [**IVideoWindow：： get \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) 方法。</span><span class="sxs-lookup"><span data-stu-id="fb401-112">This member function implements the [**IVideoWindow::get\_BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) method.</span></span> <span data-ttu-id="fb401-113">如果影片將會在另一個應用程式或檔中播放，則應用程式可能會想要使用自己的調色板。</span><span class="sxs-lookup"><span data-stu-id="fb401-113">If a video will be played within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="fb401-114">它可以將此旗標設定為1，要求影片使用目前的前景調色板，而不是其本身。</span><span class="sxs-lookup"><span data-stu-id="fb401-114">It can ask that the video use the current foreground palette rather than its own by setting this flag to  1.</span></span> <span data-ttu-id="fb401-115">如果此設定為0，則視窗將會安裝並瞭解它自己慣用的調色板。</span><span class="sxs-lookup"><span data-stu-id="fb401-115">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="fb401-116">請注意，要求視窗使用不同的調色板將會造成嚴重的效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="fb401-116">Note that asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb401-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb401-117">Requirements</span></span>



| <span data-ttu-id="fb401-118">需求</span><span class="sxs-lookup"><span data-stu-id="fb401-118">Requirement</span></span> | <span data-ttu-id="fb401-119">值</span><span class="sxs-lookup"><span data-stu-id="fb401-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb401-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fb401-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fb401-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fb401-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb401-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="fb401-122">Library</span></span><br/> | <dl> <span data-ttu-id="fb401-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fb401-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb401-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb401-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb401-125">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="fb401-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




