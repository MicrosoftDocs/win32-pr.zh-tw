---
title: AxWindowsMediaPlayer. newMedia 方法
description: NewMedia 方法會傳回新媒體專案的 IWMPMedia 介面。
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- newMedia 方法 Windows Media Player
- newMedia 方法 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，newMedia 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989662"
---
# <a name="axwindowsmediaplayernewmedia-method"></a><span data-ttu-id="ae871-106">AxWindowsMediaPlayer. newMedia 方法</span><span class="sxs-lookup"><span data-stu-id="ae871-106">AxWindowsMediaPlayer.newMedia method</span></span>

<span data-ttu-id="ae871-107">NewMedia 方法會傳回新媒體專案的 IWMPMedia 介面。</span><span class="sxs-lookup"><span data-stu-id="ae871-107">The newMedia method returns an IWMPMedia interface for a new media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae871-108">語法</span><span class="sxs-lookup"><span data-stu-id="ae871-108">Syntax</span></span>


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a><span data-ttu-id="ae871-109">參數</span><span class="sxs-lookup"><span data-stu-id="ae871-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae871-110">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="ae871-110">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="ae871-111">**System.string** ，此為用來初始化新媒體專案之數位媒體檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="ae871-111">A **System.String** that is the URL of the digital media file that is used to initialize the new media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae871-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae871-112">Return value</span></span>

<span data-ttu-id="ae871-113">表示新建立之媒體專案的 WMPLib IWMPMedia 介面。</span><span class="sxs-lookup"><span data-stu-id="ae871-113">A WMPLib.IWMPMedia interface that represents the newly created media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae871-114">備註</span><span class="sxs-lookup"><span data-stu-id="ae871-114">Remarks</span></span>

<span data-ttu-id="ae871-115">*BstrURL* 參數不得為長度為零的字串 ( "" ) 或 null。</span><span class="sxs-lookup"><span data-stu-id="ae871-115">The *bstrURL* parameter must not be a zero-length string ("") or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae871-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae871-116">Requirements</span></span>



| <span data-ttu-id="ae871-117">需求</span><span class="sxs-lookup"><span data-stu-id="ae871-117">Requirement</span></span> | <span data-ttu-id="ae871-118">值</span><span class="sxs-lookup"><span data-stu-id="ae871-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae871-119">版本</span><span class="sxs-lookup"><span data-stu-id="ae871-119">Version</span></span><br/>   | <span data-ttu-id="ae871-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="ae871-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ae871-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="ae871-121">Namespace</span></span><br/> | <span data-ttu-id="ae871-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ae871-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ae871-123">組件</span><span class="sxs-lookup"><span data-stu-id="ae871-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ae871-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="ae871-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae871-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae871-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae871-126">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ae871-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ae871-127">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ae871-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





