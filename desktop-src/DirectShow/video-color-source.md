---
description: 影片色彩來源
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: 影片色彩來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331640a9240ef0ea16ff565180503066f22ce5ae2550fa1e1ec524dcf05c8fa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071932"
---
# <a name="video-color-source"></a>影片色彩來源

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

影片色彩來源會建立純色的連續影片影像。

類別識別碼 (CLSID) ： **{0CFDD070-581A-11D2-9EE6-006008039E37}**

CLSID 變數名稱： **clsid \_ ColorSource**

屬性



| 屬性 | 類型      | 預設 | 描述                                   |
|----------|-----------|---------|-----------------------------------------------|
| 色彩  | **DWORD** | 0       | 指定要產生的色彩。 請參閱＜備註＞。 |



 

## <a name="remarks"></a>備註

影片色彩來源與來源物件搭配使用。 首先，建立新的來源物件。 然後藉 \_ 由呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法，將來源物件的子物件 GUID 設定為 CLSID ColorSource。

若要設定色彩，請建立 [屬性 Setter](property-setter.md) 物件，並在時間零套用 "color" 屬性。 這個屬性的值是 *0xAARRGGBB* 格式的十六進位數位，其中 *AA* 是 Alpha 值、 *RR* 是紅色值、 *GG* 是綠色值，而 *BB* 是藍色值。 Alpha 值的範圍從 0x00 (透明) 到 0xFF (不透明) 。 屬性是靜態的，且必須套用於時為零。

如果您未指定 Alpha 值，則預設為零 (透明) 。 在32位顏色的影片專案中，這會導致使用 Alpha 的轉換或效果，以完全透明的方式將影片色彩來源轉譯。 為了安全起見，請一律指定 Alpha。 例如，不透明的黑色是 **0xFF000000**。

下列程式碼範例顯示如何使用這個物件。 如需使用 [**IPropertySetter**](ipropertysetter.md)的詳細資訊，請參閱 [設定效果和轉換的屬性](setting-properties-on-effects-and-transitions.md)：


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



下列範例顯示在上一個範例中建立之物件的 XML 標記法。 在此情況下， [**param**](param-element.md) 元素不支援 [**at**](at-element.md) 或 [**線性**](linear-element.md) 元素，因為物件不支援動態屬性：


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



