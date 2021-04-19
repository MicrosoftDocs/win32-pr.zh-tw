---
title: IWMPSettings baseURL 屬性
description: BaseURL 屬性會取得或設定基底 URL，以用於以數位媒體內容內嵌之 URL 指令碼命令的相對路徑解析。
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- baseURL 屬性 Windows Media Player
- baseURL 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，baseURL 屬性
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976546"
---
# <a name="iwmpsettingsbaseurl-property"></a><span data-ttu-id="35711-106">IWMPSettings：： baseURL 屬性</span><span class="sxs-lookup"><span data-stu-id="35711-106">IWMPSettings::baseURL property</span></span>

<span data-ttu-id="35711-107">**BaseURL** 屬性會取得或設定基底 URL，以用於以數位媒體內容內嵌之 URL 指令碼命令的相對路徑解析。</span><span class="sxs-lookup"><span data-stu-id="35711-107">The **baseURL** property gets or sets the base URL used for relative path resolution with URL script commands that are embedded in digital media content.</span></span>

## <a name="syntax"></a><span data-ttu-id="35711-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="35711-108">Syntax</span></span>


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="35711-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="35711-109">Property value</span></span>

<span data-ttu-id="35711-110">作為基底 URL 的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="35711-110">A **System.String** that is the base URL.</span></span>

## <a name="remarks"></a><span data-ttu-id="35711-111">備註</span><span class="sxs-lookup"><span data-stu-id="35711-111">Remarks</span></span>

<span data-ttu-id="35711-112">這個屬性會指定 **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** 事件以命令參數形式傳遞的基底 HTTP URL。</span><span class="sxs-lookup"><span data-stu-id="35711-112">This property specifies the base HTTP URL that is passed as the command parameter by the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span> <span data-ttu-id="35711-113">基底 URL 會與相對 URL 串連，如下所示：</span><span class="sxs-lookup"><span data-stu-id="35711-113">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="35711-114">尾端正斜線 (/) 會加入 **baseURL** 屬性所抓取的值中。</span><span class="sxs-lookup"><span data-stu-id="35711-114">A trailing forward slash (/) is added to the value retrieved by the **baseURL** property.</span></span>
2.  <span data-ttu-id="35711-115">前置句點、反斜線或正斜線字元 (.、 \\ 和/) 會從相對 URL 中刪除。</span><span class="sxs-lookup"><span data-stu-id="35711-115">A leading period, backward slash, or forward slash character (., \\, and /) is deleted from the relative URL.</span></span>
3.  <span data-ttu-id="35711-116">相對 URL 會新增至基底 URL 的結尾。</span><span class="sxs-lookup"><span data-stu-id="35711-116">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="35711-117">產生的完整 URL 中的所有斜線字元都會指向相同方向 (轉換成正斜線或反斜線) 根據新 URL 中遇到的第一個斜線字元的方向。</span><span class="sxs-lookup"><span data-stu-id="35711-117">All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="35711-118">**注意**</span><span class="sxs-lookup"><span data-stu-id="35711-118">**Note**</span></span>

<span data-ttu-id="35711-119">Windows Media Player 控制項不支援使用兩個句號 (。在相對 URL 中 ) ，表示目前位置的父系。</span><span class="sxs-lookup"><span data-stu-id="35711-119">The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

## <a name="requirements"></a><span data-ttu-id="35711-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="35711-120">Requirements</span></span>



| <span data-ttu-id="35711-121">需求</span><span class="sxs-lookup"><span data-stu-id="35711-121">Requirement</span></span> | <span data-ttu-id="35711-122">值</span><span class="sxs-lookup"><span data-stu-id="35711-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35711-123">版本</span><span class="sxs-lookup"><span data-stu-id="35711-123">Version</span></span><br/>   | <span data-ttu-id="35711-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="35711-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="35711-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="35711-125">Namespace</span></span><br/> | <span data-ttu-id="35711-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="35711-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="35711-127">組件</span><span class="sxs-lookup"><span data-stu-id="35711-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="35711-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="35711-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35711-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35711-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35711-130">**AxWindowsMediaPlayer ScriptCommand 事件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="35711-130">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="35711-131">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="35711-131">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





