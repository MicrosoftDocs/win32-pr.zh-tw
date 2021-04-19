---
title: IWMPClosedCaption2 getSAMIStyleName 方法
description: GetSAMIStyleName 方法會傳回目前的薩米文檔案所支援的樣式名稱。
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- getSAMIStyleName 方法 Windows Media Player
- getSAMIStyleName 方法 Windows Media Player，IWMPClosedCaption2 介面
- IWMPClosedCaption2 介面 Windows Media Player，getSAMIStyleName 方法
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991210"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a><span data-ttu-id="91838-106">IWMPClosedCaption2：： getSAMIStyleName 方法</span><span class="sxs-lookup"><span data-stu-id="91838-106">IWMPClosedCaption2::getSAMIStyleName method</span></span>

<span data-ttu-id="91838-107">**GetSAMIStyleName** 方法會傳回目前的薩米文檔案所支援的樣式名稱。</span><span class="sxs-lookup"><span data-stu-id="91838-107">The **getSAMIStyleName** method returns the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="91838-108">語法</span><span class="sxs-lookup"><span data-stu-id="91838-108">Syntax</span></span>


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a><span data-ttu-id="91838-109">參數</span><span class="sxs-lookup"><span data-stu-id="91838-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91838-110">*nIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91838-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91838-111">要抓取之樣式名稱以零為基底之索引的 **system.object。**</span><span class="sxs-lookup"><span data-stu-id="91838-111">A **System.Int32** that is the zero-based index of the style name to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91838-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="91838-112">Return value</span></span>

<span data-ttu-id="91838-113">**System.string** ，這是以薩米文檔案指定的樣式名稱。</span><span class="sxs-lookup"><span data-stu-id="91838-113">A **System.String** that is the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="91838-114">備註</span><span class="sxs-lookup"><span data-stu-id="91838-114">Remarks</span></span>

<span data-ttu-id="91838-115">薩米文檔案中的樣式會依照檔案中顯示的順序編制索引，從零開始。</span><span class="sxs-lookup"><span data-stu-id="91838-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="91838-116">除非數位媒體檔案已開啟 (AxWindowsMediaPlayer，否則這個方法會傳回長度為零的字串 ( "" ) 。 openState 等於 13) 。</span><span class="sxs-lookup"><span data-stu-id="91838-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="91838-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="91838-117">Requirements</span></span>



| <span data-ttu-id="91838-118">需求</span><span class="sxs-lookup"><span data-stu-id="91838-118">Requirement</span></span> | <span data-ttu-id="91838-119">值</span><span class="sxs-lookup"><span data-stu-id="91838-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91838-120">版本</span><span class="sxs-lookup"><span data-stu-id="91838-120">Version</span></span><br/>   | <span data-ttu-id="91838-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="91838-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="91838-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="91838-122">Namespace</span></span><br/> | <span data-ttu-id="91838-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="91838-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="91838-124">組件</span><span class="sxs-lookup"><span data-stu-id="91838-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="91838-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="91838-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91838-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91838-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91838-127">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="91838-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="91838-128">**IWMPClosedCaption 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="91838-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91838-129">**IWMPClosedCaption. SAMIStyle (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="91838-129">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91838-130">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="91838-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





