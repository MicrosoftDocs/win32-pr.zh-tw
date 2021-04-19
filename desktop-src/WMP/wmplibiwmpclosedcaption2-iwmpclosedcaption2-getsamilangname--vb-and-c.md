---
title: IWMPClosedCaption2 getSAMILangName 方法
description: GetSAMILangName 方法會傳回目前的薩米文檔案所支援的語言名稱。
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- getSAMILangName 方法 Windows Media Player
- getSAMILangName 方法 Windows Media Player，IWMPClosedCaption2 介面
- IWMPClosedCaption2 介面 Windows Media Player，getSAMILangName 方法
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000477"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a><span data-ttu-id="2b097-106">IWMPClosedCaption2：： getSAMILangName 方法</span><span class="sxs-lookup"><span data-stu-id="2b097-106">IWMPClosedCaption2::getSAMILangName method</span></span>

<span data-ttu-id="2b097-107">**GetSAMILangName** 方法會傳回目前的薩米文檔案所支援的語言名稱。</span><span class="sxs-lookup"><span data-stu-id="2b097-107">The **getSAMILangName** method returns the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b097-108">語法</span><span class="sxs-lookup"><span data-stu-id="2b097-108">Syntax</span></span>


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a><span data-ttu-id="2b097-109">參數</span><span class="sxs-lookup"><span data-stu-id="2b097-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b097-110">*nIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b097-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b097-111">要抓取之語言名稱以零為基底之索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="2b097-111">**A System.Int32** that is the zero-based index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b097-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b097-112">Return value</span></span>

<span data-ttu-id="2b097-113">**System.string** ，這是以薩米文檔案指定的語言名稱。</span><span class="sxs-lookup"><span data-stu-id="2b097-113">A **System.String** that is the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b097-114">備註</span><span class="sxs-lookup"><span data-stu-id="2b097-114">Remarks</span></span>

<span data-ttu-id="2b097-115">薩米文檔案中的語言會依照檔案中顯示的順序編制索引，從零開始。</span><span class="sxs-lookup"><span data-stu-id="2b097-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="2b097-116">除非數位媒體檔案已開啟 (AxWindowsMediaPlayer，否則這個方法會傳回長度為零的字串 ( "" ) 。 openState 等於 13) 。</span><span class="sxs-lookup"><span data-stu-id="2b097-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b097-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b097-117">Requirements</span></span>



| <span data-ttu-id="2b097-118">需求</span><span class="sxs-lookup"><span data-stu-id="2b097-118">Requirement</span></span> | <span data-ttu-id="2b097-119">值</span><span class="sxs-lookup"><span data-stu-id="2b097-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b097-120">版本</span><span class="sxs-lookup"><span data-stu-id="2b097-120">Version</span></span><br/>   | <span data-ttu-id="2b097-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="2b097-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2b097-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="2b097-122">Namespace</span></span><br/> | <span data-ttu-id="2b097-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2b097-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2b097-124">組件</span><span class="sxs-lookup"><span data-stu-id="2b097-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2b097-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="2b097-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b097-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b097-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b097-127">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="2b097-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="2b097-128">**IWMPClosedCaption 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2b097-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b097-129">**IWMPClosedCaption. SAMILang (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2b097-129">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b097-130">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2b097-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





