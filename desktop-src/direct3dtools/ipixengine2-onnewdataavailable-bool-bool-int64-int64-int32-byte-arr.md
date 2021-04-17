---
description: 要求指出圖形記錄檔中有新的資料。
MS-HAID: vspixengine.IPixEngine2\_OnNewDataAvailable\_BOOL\_BOOL\_INT64\_INT64\_INT32\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2：： OnNewDataAvailable 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B99FC54C-9395-4B14-93D5-B6408D655DC3
api_name:
- IPixEngine2.OnNewDataAvailable
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3de880153eec5b41849167f3a87a3f77f31aeffd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510043"
---
# <a name="span-idvspixengineipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arrspanipixengine2onnewdataavailable-method"></a><span data-ttu-id="a2d25-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2：： OnNewDataAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="a2d25-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2::OnNewDataAvailable method</span></span>

<span data-ttu-id="a2d25-104">要求指出圖形記錄檔中有新的資料。</span><span class="sxs-lookup"><span data-stu-id="a2d25-104">Requests to indicate that the graphics log has new data inside of it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d25-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2d25-105">Syntax</span></span>


```C++
HRESULT OnNewDataAvailable(
   BOOL    fSessionEnd,
   BOOL    fUnloadCurFrame,
   INT64   i64FilePositionStart,
   INT64   i64FilePositionEnd,
   INT32   iObjectTableDataSize,
   BYTE [] count4_pObjectTableData
);
```

## <a name="parameters"></a><span data-ttu-id="a2d25-106">參數</span><span class="sxs-lookup"><span data-stu-id="a2d25-106">Parameters</span></span>

<span data-ttu-id="a2d25-107">*fSessionEnd* </span><span class="sxs-lookup"><span data-stu-id="a2d25-107">*fSessionEnd* </span></span>  
<span data-ttu-id="a2d25-108">如果會話已結束，則為 true，否則為 false。</span><span class="sxs-lookup"><span data-stu-id="a2d25-108">true if the session has ended, otherwise false.</span></span>

<span data-ttu-id="a2d25-109">*fUnloadCurFrame* </span><span class="sxs-lookup"><span data-stu-id="a2d25-109">*fUnloadCurFrame* </span></span>  
<span data-ttu-id="a2d25-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="a2d25-110">Not used.</span></span>

<span data-ttu-id="a2d25-111">*i64FilePositionStart* </span><span class="sxs-lookup"><span data-stu-id="a2d25-111">*i64FilePositionStart* </span></span>  
<span data-ttu-id="a2d25-112">新資料開始的檔案位置（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2d25-112">The file position, in bytes, at which the new data begins.</span></span>

<span data-ttu-id="a2d25-113">*i64FilePositionEnd* </span><span class="sxs-lookup"><span data-stu-id="a2d25-113">*i64FilePositionEnd* </span></span>  
<span data-ttu-id="a2d25-114">新資料的結束位置（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2d25-114">The file position, in bytes, at which the new data ends.</span></span>

<span data-ttu-id="a2d25-115">*iObjectTableDataSize* </span><span class="sxs-lookup"><span data-stu-id="a2d25-115">*iObjectTableDataSize* </span></span>  
<span data-ttu-id="a2d25-116">Count4 pObjectTableData 中包含的位元組數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a2d25-116">The number of bytes contained in count4\_pObjectTableData.</span></span>

<span data-ttu-id="a2d25-117">*count4 \_ pObjectTableData* </span><span class="sxs-lookup"><span data-stu-id="a2d25-117">*count4\_pObjectTableData* </span></span>  
<span data-ttu-id="a2d25-118">包含物件資料表之資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a2d25-118">An buffer containing data for the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2d25-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2d25-119">Return value</span></span>

<span data-ttu-id="a2d25-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a2d25-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2d25-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a2d25-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2d25-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2d25-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a2d25-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a2d25-123">Header</span></span></p></td><td><span data-ttu-id="a2d25-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a2d25-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a2d25-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2d25-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a2d25-126">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="a2d25-126">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
