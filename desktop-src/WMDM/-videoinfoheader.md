---
title: _VIDEOINFOHEADER 結構
description: '\_VIDEOINFOHEADER 結構包含影片串流的相關資訊，並包含 \_ 定義個別框架格式的 BITMAPINFOHEADER 結構。'
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982264"
---
# <a name="_videoinfoheader-structure"></a><span data-ttu-id="45253-104">\_VIDEOINFOHEADER 結構</span><span class="sxs-lookup"><span data-stu-id="45253-104">\_VIDEOINFOHEADER structure</span></span>

<span data-ttu-id="45253-105">**\_ VIDEOINFOHEADER** 結構包含影片串流的相關資訊，並包含定義個別框架格式的 **\_ BITMAPINFOHEADER** 結構。</span><span class="sxs-lookup"><span data-stu-id="45253-105">The **\_VIDEOINFOHEADER** structure contains information about a video stream and includes a **\_BITMAPINFOHEADER** structure that defines the format of an individual frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="45253-106">語法</span><span class="sxs-lookup"><span data-stu-id="45253-106">Syntax</span></span>


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="45253-107">成員</span><span class="sxs-lookup"><span data-stu-id="45253-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="45253-108">**rcSource**</span><span class="sxs-lookup"><span data-stu-id="45253-108">**rcSource**</span></span>
</dt> <dd>

<span data-ttu-id="45253-109">指定來源影片視窗的 **RECT** 結構。</span><span class="sxs-lookup"><span data-stu-id="45253-109">**RECT** structure that specifies the source video window.</span></span>

</dd> <dt>

<span data-ttu-id="45253-110">**rcTarget**</span><span class="sxs-lookup"><span data-stu-id="45253-110">**rcTarget**</span></span>
</dt> <dd>

<span data-ttu-id="45253-111">指定目的地影片視窗的 **RECT** 結構。</span><span class="sxs-lookup"><span data-stu-id="45253-111">**RECT** structure that specifies the destination video window.</span></span>

</dd> <dt>

<span data-ttu-id="45253-112">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="45253-112">**dwBitRate**</span></span>
</dt> <dd>

<span data-ttu-id="45253-113">**DWORD** 值，指定影片串流的近似資料速率（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="45253-113">**DWORD** value that specifies the video stream's approximate data rate, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="45253-114">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="45253-114">**dwBitErrorRate**</span></span>
</dt> <dd>

<span data-ttu-id="45253-115">**DWORD** 值，指定影片資料流程的資料錯誤率，以每秒的位錯誤表示。</span><span class="sxs-lookup"><span data-stu-id="45253-115">**DWORD** value that specifies the video stream's data error rate, in bit errors per second.</span></span>

</dd> <dt>

<span data-ttu-id="45253-116">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="45253-116">**AvgTimePerFrame**</span></span>
</dt> <dd>

<span data-ttu-id="45253-117">**參考 \_時間** 值，指定影片框架的平均顯示時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="45253-117">**REFERENCE\_TIME** value that specifies the video frame's average display time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="45253-118">**bmiHeader**</span><span class="sxs-lookup"><span data-stu-id="45253-118">**bmiHeader**</span></span>
</dt> <dd>

<span data-ttu-id="45253-119">Win32 **\_ BITMAPINFOHEADER** 結構，其中包含影片影像點陣圖的色彩和維度資訊。</span><span class="sxs-lookup"><span data-stu-id="45253-119">Win32 **\_BITMAPINFOHEADER** structure that contains color and dimension information for the video image bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45253-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="45253-120">Requirements</span></span>



| <span data-ttu-id="45253-121">需求</span><span class="sxs-lookup"><span data-stu-id="45253-121">Requirement</span></span> | <span data-ttu-id="45253-122">值</span><span class="sxs-lookup"><span data-stu-id="45253-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="45253-123">標頭</span><span class="sxs-lookup"><span data-stu-id="45253-123">Header</span></span><br/> | <dl> <span data-ttu-id="45253-124"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="45253-124"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45253-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45253-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45253-126">**\_BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="45253-126">**\_BITMAPINFOHEADER**</span></span>](-bitmapinfoheader.md)
</dt> <dt>

[<span data-ttu-id="45253-127">**結構**</span><span class="sxs-lookup"><span data-stu-id="45253-127">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





