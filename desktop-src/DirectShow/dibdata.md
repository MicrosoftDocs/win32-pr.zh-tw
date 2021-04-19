---
description: DIBDATA 結構包含與 GDI 裝置無關的點陣圖 (DIB) 的相關資訊。
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: 'DIBDATA 結構 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985784"
---
# <a name="dibdata-structure"></a><span data-ttu-id="3bb4b-103">DIBDATA 結構</span><span class="sxs-lookup"><span data-stu-id="3bb4b-103">DIBDATA structure</span></span>

<span data-ttu-id="3bb4b-104">此 `DIBDATA` 結構包含與 GDI 裝置無關的點陣圖 (DIB) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3bb4b-104">The `DIBDATA` structure contains information about a GDI device-independent bitmap (DIB).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb4b-105">語法</span><span class="sxs-lookup"><span data-stu-id="3bb4b-105">Syntax</span></span>


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a><span data-ttu-id="3bb4b-106">成員</span><span class="sxs-lookup"><span data-stu-id="3bb4b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3bb4b-107">**PaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="3bb4b-107">**PaletteVersion**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4b-108">每當選擇區變更時，此成員應該遞增。</span><span class="sxs-lookup"><span data-stu-id="3bb4b-108">This member should be incremented whenever the palette changes.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4b-109">**DibSection**</span><span class="sxs-lookup"><span data-stu-id="3bb4b-109">**DibSection**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4b-110">**DIBSECTION** 結構，其中包含 DIB 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3bb4b-110">**DIBSECTION** structure that contains information about the DIB.</span></span> <span data-ttu-id="3bb4b-111">請參閱 GDI 檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bb4b-111">See the GDI documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4b-112">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="3bb4b-112">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4b-113">點陣圖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3bb4b-113">Handle to the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4b-114">**hMapping**</span><span class="sxs-lookup"><span data-stu-id="3bb4b-114">**hMapping**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4b-115">檔案對應物件的控制碼，這個物件是用來共用 GDI 與 [**CImageSample**](cimagesample.md) 物件之間的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3bb4b-115">Handle to a file-mapping object that is used to share memory between GDI and a [**CImageSample**](cimagesample.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4b-116">**pBase**</span><span class="sxs-lookup"><span data-stu-id="3bb4b-116">**pBase**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4b-117">點陣圖的位址。</span><span class="sxs-lookup"><span data-stu-id="3bb4b-117">Address of the bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bb4b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bb4b-118">Requirements</span></span>



| <span data-ttu-id="3bb4b-119">需求</span><span class="sxs-lookup"><span data-stu-id="3bb4b-119">Requirement</span></span> | <span data-ttu-id="3bb4b-120">值</span><span class="sxs-lookup"><span data-stu-id="3bb4b-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb4b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3bb4b-121">Header</span></span><br/> | <dl> <span data-ttu-id="3bb4b-122"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3bb4b-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl> |



 

 




