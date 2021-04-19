---
description: MakeIdentityPalette 方法會嘗試建立 &\# 0034; 身分識別選擇區 &\# 0034; 定義為直接對應至顯示裝置中所選取之調色板的識別碼。
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: 'CImagePalette. MakeIdentityPalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994180"
---
# <a name="cimagepalettemakeidentitypalette-method"></a><span data-ttu-id="d3044-103">CImagePalette. MakeIdentityPalette 方法</span><span class="sxs-lookup"><span data-stu-id="d3044-103">CImagePalette.MakeIdentityPalette method</span></span>

<span data-ttu-id="d3044-104">方法會嘗試將「身分識別選擇區」 `MakeIdentityPalette` 定義為直接對應至顯示裝置中所選取之調色板的元件。</span><span class="sxs-lookup"><span data-stu-id="d3044-104">The `MakeIdentityPalette` method attempts to make an "identity palette," defined as one that maps directly to the palette selected in the display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3044-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3044-105">Syntax</span></span>


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d3044-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3044-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3044-107">*pEntry*</span><span class="sxs-lookup"><span data-stu-id="d3044-107">*pEntry*</span></span> 
</dt> <dd>

<span data-ttu-id="d3044-108">元件專案陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="d3044-108">Pointer to an array of palette entries.</span></span>

</dd> <dt>

<span data-ttu-id="d3044-109">*iColours*</span><span class="sxs-lookup"><span data-stu-id="d3044-109">*iColours*</span></span> 
</dt> <dd>

<span data-ttu-id="d3044-110">*PEntry* 中的調色板專案數目。</span><span class="sxs-lookup"><span data-stu-id="d3044-110">Number of palette entries in *pEntry*.</span></span>

</dd> <dt>

<span data-ttu-id="d3044-111">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="d3044-111">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d3044-112">字串的指標，其中包含由 GDI **EnumDisplayDevices** 函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3044-112">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="d3044-113">若要使用主顯示器裝置，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d3044-113">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3044-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3044-114">Return value</span></span>

<span data-ttu-id="d3044-115">\_如果成功，則傳回 s OK \_ ，如果失敗，則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="d3044-115">Returns S\_OK if successful or S\_FALSE if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3044-116">備註</span><span class="sxs-lookup"><span data-stu-id="d3044-116">Remarks</span></span>

<span data-ttu-id="d3044-117">這個方法會比較系統元件中的保留專案與 *pEntry* 陣列中的對應專案。</span><span class="sxs-lookup"><span data-stu-id="d3044-117">This method compares the reserved entries in the system palette against the corresponding entries in the *pEntry* array.</span></span> <span data-ttu-id="d3044-118">如果它們完全相符，則方法會 \_ 在 *pEntry* 的其餘 (非保留) 的調色板專案中，設定電腦 NOCOLLAPSE 旗標。</span><span class="sxs-lookup"><span data-stu-id="d3044-118">If they match exactly, the method sets the PC\_NOCOLLAPSE flag in the remaining (non-reserved) palette entries in *pEntry*.</span></span> <span data-ttu-id="d3044-119">此旗標會防止 GDI 嘗試將邏輯調色板專案對應至系統元件專案。</span><span class="sxs-lookup"><span data-stu-id="d3044-119">This flag prevents GDI from trying map logical palette entries to system palette entries.</span></span>

<span data-ttu-id="d3044-120">[**CImagePalette：： MakePalette**](cimagepalette-makepalette.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d3044-120">The [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3044-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3044-121">Requirements</span></span>



| <span data-ttu-id="d3044-122">需求</span><span class="sxs-lookup"><span data-stu-id="d3044-122">Requirement</span></span> | <span data-ttu-id="d3044-123">值</span><span class="sxs-lookup"><span data-stu-id="d3044-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3044-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d3044-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d3044-125"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d3044-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3044-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3044-126">Library</span></span><br/> | <dl> <span data-ttu-id="d3044-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d3044-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3044-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3044-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3044-129">**CImagePalette 類別**</span><span class="sxs-lookup"><span data-stu-id="d3044-129">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




