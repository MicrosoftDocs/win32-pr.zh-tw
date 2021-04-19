---
title: IWMPClosedCaption2 getSAMILangID 方法
description: GetSAMILangID 方法會傳回目前薩米文檔案所支援語言 (LCID) 的地區設定識別碼。
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- getSAMILangID 方法 Windows Media Player
- getSAMILangID 方法 Windows Media Player，IWMPClosedCaption2 介面
- IWMPClosedCaption2 介面 Windows Media Player，getSAMILangID 方法
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987942"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a><span data-ttu-id="6086c-106">IWMPClosedCaption2：： getSAMILangID 方法</span><span class="sxs-lookup"><span data-stu-id="6086c-106">IWMPClosedCaption2::getSAMILangID method</span></span>

<span data-ttu-id="6086c-107">**GetSAMILangID** 方法會傳回目前薩米文檔案所支援語言 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="6086c-107">The **getSAMILangID** method returns the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6086c-108">語法</span><span class="sxs-lookup"><span data-stu-id="6086c-108">Syntax</span></span>


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a><span data-ttu-id="6086c-109">參數</span><span class="sxs-lookup"><span data-stu-id="6086c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6086c-110">*nIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6086c-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6086c-111">要抓取之 LCID 的以零為基底之索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="6086c-111">A **System.Int32** that is the zero-based index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6086c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6086c-112">Return value</span></span>

<span data-ttu-id="6086c-113">使用指定索引之語言的 LCID 的 **system.object。**</span><span class="sxs-lookup"><span data-stu-id="6086c-113">A **System.Int32** that is the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="6086c-114">備註</span><span class="sxs-lookup"><span data-stu-id="6086c-114">Remarks</span></span>

<span data-ttu-id="6086c-115">薩米文檔案中的語言會依照檔案中顯示的順序編制索引，從零開始。</span><span class="sxs-lookup"><span data-stu-id="6086c-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="6086c-116">除非 (AxWindowsMediaPlayer 開啟數位媒體檔案，否則這個方法會傳回0。 openState 等於 13) 。</span><span class="sxs-lookup"><span data-stu-id="6086c-116">This method returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="6086c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6086c-117">Requirements</span></span>



| <span data-ttu-id="6086c-118">需求</span><span class="sxs-lookup"><span data-stu-id="6086c-118">Requirement</span></span> | <span data-ttu-id="6086c-119">值</span><span class="sxs-lookup"><span data-stu-id="6086c-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6086c-120">版本</span><span class="sxs-lookup"><span data-stu-id="6086c-120">Version</span></span><br/>   | <span data-ttu-id="6086c-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6086c-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6086c-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="6086c-122">Namespace</span></span><br/> | <span data-ttu-id="6086c-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6086c-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6086c-124">組件</span><span class="sxs-lookup"><span data-stu-id="6086c-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6086c-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6086c-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6086c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6086c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6086c-127">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="6086c-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="6086c-128">**IWMPClosedCaption 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6086c-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6086c-129">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6086c-129">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





