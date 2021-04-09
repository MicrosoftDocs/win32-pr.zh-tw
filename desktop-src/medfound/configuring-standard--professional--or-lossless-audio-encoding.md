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
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>設定標準、專業或不失真音訊編碼

當 Windows Media 音訊編碼器列舉輸出型別時，它會將每個列舉型別識別為 Standard、Professional 或無損。 您可以執行下列步驟來判斷輸出類型是標準、專業或非失真。

1.  呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 來取得代表輸出型別的 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面。
2.  呼叫 [**IMFMediaType：： GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) 以取得包含輸出類型相關資訊的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。
3.  [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的 **pbFormat** 成員會指向 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構，其中包含有關輸出類型的其他資訊。 檢查 **WAVEFORMATEX** 結構的 **wFormatTag** 成員。 0x161 的值表示標準，0x162 的值表示 Professional，而0x163 的值表示不失真。

如果您在列舉輸出類型之前，在 Windows Media 音訊編碼器上設定屬性，您可以限制列舉的輸出類型數目。 例如，如果您適當地設定 VBR 屬性，您可以將列舉的輸出類型限制為不失真分類中的型別。

## <a name="standard-audio-encoding"></a>標準音頻編碼

您可以使用下列步驟來設定標準音頻編碼。

1.  在編碼器上設定您所選擇的屬性。
2.  列舉可能的輸出類型。
3.  檢查列舉型別，然後選擇具有0x161 之音訊格式標記的類型。
4.  藉由呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)，將輸出類型設定為您選擇的類型。

## <a name="professional-audio-encoding"></a>Professional 音訊編碼

您可以使用下列步驟來設定專業音訊編碼。

1.  在編碼器上設定您所選擇的屬性。
2.  列舉可能的輸出類型。
3.  檢查列舉型別，然後選擇具有0x162 之音訊格式標記的類型。
4.  藉由呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)，將輸出類型設定為您選擇的類型。

## <a name="lossless-audio-encoding"></a>無失真音訊編碼

您可以使用下列步驟來設定不失真的音訊編碼。

1.  將 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性設定為 **VARIANT \_ TRUE**。
2.  將 [**MFPKEY \_ 限制列舉 \_ 的 \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) 屬性設定為 **VARIANT \_ TRUE**。
3.  將 [**MFPKEY \_ 所需的 \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) 屬性設定為100。
4.  列舉輸出類型。
5.  藉由呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)，將輸出類型設定為步驟4列舉的其中一個類型。

下列程式碼會列舉 Windows Media 音訊編碼器的所有不失真輸出類型。 程式碼會列印每個列舉型別的音訊格式標記值。 因為所有列舉型別都是無失真的，所以這些格式標記的所有值都是0x163。 假設 pIMT 是 Windows Media 音訊編碼器物件上 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的指標，而 pStore 是相同物件上的 **IPropertyStore** 介面指標。 也假設 hr 是在程式碼中先前宣告之 **HRESULT** 類型的變數。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定音訊編碼](configuringaudioencoding.md)
</dt> </dl>

 

 
