---
description: 當 Windows Media 音訊編碼器列舉輸出型別時，它會將每個列舉型別識別為 Standard、Professional 或無損。
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: 設定標準、專業或不失真音訊編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e781c2c093b46a12fa4ad5434f97931a948ff9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689344"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a><span data-ttu-id="33c25-103">設定標準、專業或不失真音訊編碼</span><span class="sxs-lookup"><span data-stu-id="33c25-103">Configuring Standard, Professional, or Lossless Audio Encoding</span></span>

<span data-ttu-id="33c25-104">當 Windows Media 音訊編碼器列舉輸出型別時，它會將每個列舉型別識別為 Standard、Professional 或無損。</span><span class="sxs-lookup"><span data-stu-id="33c25-104">When the Windows Media Audio encoder enumerates output types, it identifies each enumerated type as either Standard, Professional, or Lossless.</span></span> <span data-ttu-id="33c25-105">您可以執行下列步驟來判斷輸出類型是標準、專業或非失真。</span><span class="sxs-lookup"><span data-stu-id="33c25-105">You can determine whether an output type is Standard, Professional, or Lossless by performing the following steps.</span></span>

1.  <span data-ttu-id="33c25-106">呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 來取得代表輸出型別的 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面。</span><span class="sxs-lookup"><span data-stu-id="33c25-106">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to obtain an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface that represents the output type.</span></span>
2.  <span data-ttu-id="33c25-107">呼叫 [**IMFMediaType：： GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) 以取得包含輸出類型相關資訊的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="33c25-107">Call [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) to get an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains information about the output type.</span></span>
3.  <span data-ttu-id="33c25-108">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的 **pbFormat** 成員會指向 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構，其中包含有關輸出類型的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="33c25-108">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure points to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure that contains additional information about the output type.</span></span> <span data-ttu-id="33c25-109">檢查 **WAVEFORMATEX** 結構的 **wFormatTag** 成員。</span><span class="sxs-lookup"><span data-stu-id="33c25-109">Inspect the **wFormatTag** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="33c25-110">0x161 的值表示標準，0x162 的值表示 Professional，而0x163 的值表示不失真。</span><span class="sxs-lookup"><span data-stu-id="33c25-110">A value of 0x161 indicates Standard, a value of 0x162 indicates Professional, and a value of 0x163 indicates Lossless.</span></span>

<span data-ttu-id="33c25-111">如果您在列舉輸出類型之前，在 Windows Media 音訊編碼器上設定屬性，您可以限制列舉的輸出類型數目。</span><span class="sxs-lookup"><span data-stu-id="33c25-111">If you set properties on the Windows Media Audio encoder before you enumerate output types, you can limit the number of output types that are enumerated.</span></span> <span data-ttu-id="33c25-112">例如，如果您適當地設定 VBR 屬性，您可以將列舉的輸出類型限制為不失真分類中的型別。</span><span class="sxs-lookup"><span data-stu-id="33c25-112">For example, if you set the VBR properties appropriately, you can limit the enumerated output types to those that are in the Lossless category.</span></span>

## <a name="standard-audio-encoding"></a><span data-ttu-id="33c25-113">標準音頻編碼</span><span class="sxs-lookup"><span data-stu-id="33c25-113">Standard Audio Encoding</span></span>

<span data-ttu-id="33c25-114">您可以使用下列步驟來設定標準音頻編碼。</span><span class="sxs-lookup"><span data-stu-id="33c25-114">You can use the following steps to configure Standard audio encoding.</span></span>

1.  <span data-ttu-id="33c25-115">在編碼器上設定您所選擇的屬性。</span><span class="sxs-lookup"><span data-stu-id="33c25-115">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="33c25-116">列舉可能的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="33c25-116">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="33c25-117">檢查列舉型別，然後選擇具有0x161 之音訊格式標記的類型。</span><span class="sxs-lookup"><span data-stu-id="33c25-117">Inspect the enumerated types and choose one that has an audio format tag of 0x161.</span></span>
4.  <span data-ttu-id="33c25-118">藉由呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)，將輸出類型設定為您選擇的類型。</span><span class="sxs-lookup"><span data-stu-id="33c25-118">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="professional-audio-encoding"></a><span data-ttu-id="33c25-119">Professional 音訊編碼</span><span class="sxs-lookup"><span data-stu-id="33c25-119">Professional Audio Encoding</span></span>

<span data-ttu-id="33c25-120">您可以使用下列步驟來設定專業音訊編碼。</span><span class="sxs-lookup"><span data-stu-id="33c25-120">You can use the following steps to configure Professional audio encoding.</span></span>

1.  <span data-ttu-id="33c25-121">在編碼器上設定您所選擇的屬性。</span><span class="sxs-lookup"><span data-stu-id="33c25-121">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="33c25-122">列舉可能的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="33c25-122">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="33c25-123">檢查列舉型別，然後選擇具有0x162 之音訊格式標記的類型。</span><span class="sxs-lookup"><span data-stu-id="33c25-123">Inspect the enumerated types and choose one that has an audio format tag of 0x162.</span></span>
4.  <span data-ttu-id="33c25-124">藉由呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)，將輸出類型設定為您選擇的類型。</span><span class="sxs-lookup"><span data-stu-id="33c25-124">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="lossless-audio-encoding"></a><span data-ttu-id="33c25-125">無失真音訊編碼</span><span class="sxs-lookup"><span data-stu-id="33c25-125">Lossless Audio Encoding</span></span>

<span data-ttu-id="33c25-126">您可以使用下列步驟來設定不失真的音訊編碼。</span><span class="sxs-lookup"><span data-stu-id="33c25-126">You can use the following steps to configure Lossless audio encoding.</span></span>

1.  <span data-ttu-id="33c25-127">將 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="33c25-127">Set the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to **VARIANT\_TRUE**.</span></span>
2.  <span data-ttu-id="33c25-128">將 [**MFPKEY \_ 限制列舉 \_ 的 \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) 屬性設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="33c25-128">Set the [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) property to **VARIANT\_TRUE**.</span></span>
3.  <span data-ttu-id="33c25-129">將 [**MFPKEY \_ 所需的 \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) 屬性設定為100。</span><span class="sxs-lookup"><span data-stu-id="33c25-129">Set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property to 100.</span></span>
4.  <span data-ttu-id="33c25-130">列舉輸出類型。</span><span class="sxs-lookup"><span data-stu-id="33c25-130">Enumerate output types.</span></span>
5.  <span data-ttu-id="33c25-131">藉由呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)，將輸出類型設定為步驟4列舉的其中一個類型。</span><span class="sxs-lookup"><span data-stu-id="33c25-131">Set the output type to one of the types enumerated in step 4 by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="33c25-132">下列程式碼會列舉 Windows Media 音訊編碼器的所有不失真輸出類型。</span><span class="sxs-lookup"><span data-stu-id="33c25-132">The following code enumerates all of the lossless output types for the Windows Media Audio encoder.</span></span> <span data-ttu-id="33c25-133">程式碼會列印每個列舉型別的音訊格式標記值。</span><span class="sxs-lookup"><span data-stu-id="33c25-133">The code prints the value of the audio format tag for each enumerated type.</span></span> <span data-ttu-id="33c25-134">因為所有列舉型別都是無失真的，所以這些格式標記的所有值都是0x163。</span><span class="sxs-lookup"><span data-stu-id="33c25-134">Because all of the enumerated types are lossless, all of those format tags have a value of 0x163.</span></span> <span data-ttu-id="33c25-135">假設 pIMT 是 Windows Media 音訊編碼器物件上 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的指標，而 pStore 是相同物件上的 **IPropertyStore** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="33c25-135">Assume that pIMT is a pointer to an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a Windows Media Audio encoder object and that pStore is a pointer to an **IPropertyStore** interface on the same object.</span></span> <span data-ttu-id="33c25-136">也假設 hr 是在程式碼中先前宣告之 **HRESULT** 類型的變數。</span><span class="sxs-lookup"><span data-stu-id="33c25-136">Also assume that hr is a variable of type **HRESULT** that was declared previously in the code.</span></span>


```
PROPVARIANT prop;
prop.vt = VT_BOOL;
prop.boolVal = VARIANT_TRUE;
hr = pStore->SetValue(MFPKEY_VBRENABLED, prop);

if(SUCCEEDED(hr))
{
   hr = pStore->SetValue(MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, prop);

   if(SUCCEEDED(hr))
   {
      prop.vt = VT_UI4;
      prop.ulVal = 100;
      hr = pStore->SetValue(MFPKEY_DESIRED_VBRQUALITY, prop);
      
      if(SUCCEEDED(hr))
      {           
         HRESULT hrAvailableType = S_OK;
         LONG j = 0;
         while(MF_E_NO_MORE_TYPES != hrAvailableType)
         {
            IMFMediaType* pOutputType = NULL;     
            hrAvailableType = pIMFT->GetOutputAvailableType(
               0, j, &pOutputType);

            if(SUCCEEDED(hrAvailableType))
            {
               AM_MEDIA_TYPE* pTypeRep = NULL;
               hr = pOutputType->GetRepresentation(
                  AM_MEDIA_TYPE_REPRESENTATION, (VOID**)&pTypeRep); 
                     
               if(SUCCEEDED(hr))
               {
                  WAVEFORMATEX* pwfex = (WAVEFORMATEX*)pTypeRep->pbFormat;
                  printf_s("%x\n", pwfex->wFormatTag);
                  pOutputType->FreeRepresentation(
                     AM_MEDIA_TYPE_REPRESENTATION, (VOID*)pTypeRep);
               }

               pOutputType->Release();
               ++j;
            }                                                                  
         } // while                 
      }                                
   } 
}
```



## <a name="related-topics"></a><span data-ttu-id="33c25-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="33c25-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33c25-138">設定音訊編碼</span><span class="sxs-lookup"><span data-stu-id="33c25-138">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> </dl>

 

 
