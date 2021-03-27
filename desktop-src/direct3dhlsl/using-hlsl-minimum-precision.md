---
title: 使用 HLSL 最小有效位數
description: 從 Windows 8 開始，圖形驅動程式可以使用任何有效位數大於或等於指定的位精確度，來執行最小有效位數 HLSL 純量資料類型。
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7f66f35aef3e870edb4e8564a280be89ce34be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682574"
---
# <a name="using-hlsl-minimum-precision"></a>使用 HLSL 最小有效位數

從 Windows 8 開始，圖形驅動程式可以使用任何有效位數大於或等於指定的位精確度，來執行最小有效位數 HLSL 純量 [資料類型](dx-graphics-hlsl-scalar.md) 。 當您的 HLSL 最小精確度著色器程式碼在實 HLSL 最小精確度的硬體上使用時，您會使用較少的記憶體頻寬，因此您也會使用較少的系統電源。

您可以藉由呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) 與 [**D3D11 \_ 功能 \_ 著色器的 \_ 最小 \_ 精確度 \_ 支援**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) 值，來查詢圖形驅動程式所提供的最小精確度支援。 如需詳細資訊，請參閱 [HLSL 最小精確度支援](/windows/desktop/direct3d11/direct3d-11-1-features)。

-   [宣告具有最小精確度資料類型的變數](#declare-variables-with-minimum-precision-data-types)
-   [測試最小精確度著色器程式碼](#testing-your-minimum-precision-shader-code)
-   [相關主題](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a>宣告具有最小精確度資料類型的變數

若要在 HLSL 著色器程式碼中使用最小有效位數，請針對向量) 、 **min16int**、 **min10float** 等類型宣告個別變數，例如 **min16float** (**min16float4** 。 使用這些變數時，您的著色器程式碼表示它不需要比變數所指出更多的精確度。 但硬體可以忽略最小精確度指標，並以完整的32位精確度執行。 當您在採用最小精確度的硬體上使用您的著色器程式碼時，您會使用較少的記憶體頻寬，因此，只要您的著色器程式碼不會預期比指定的精確，您也會使用較少的系統電源。

您不需要撰寫多個執行和不使用最小精確度的著色器。 相反地，如果圖形驅動程式回報不支援任何最小有效位數，則建立具有最小精確度的著色器，且最小精確度變數的行為會是完整的32位有效位數。 HLSL 最小精確度著色器無法在早于 Windows 8 的作業系統上運作，因此，如果您打算以較早的作業系統為目標，則必須撰寫多個著色器，有些會執行，有些則不會使用最小有效位數。

> [!Note]  
> 請勿在著色器內的不同精確度層級之間進行資料切換，因為這些類型的轉換會浪費和降低效能。 唯一的例外是，著色器常數仍一律為32位，但廠商可以設計圖形硬體，以自由地關閉轉換成 HLSL 指令讀取可能使用的精確度。

 

藉由使用最小有效位數，您可以在著色器程式碼的各個部分中控制計算的精確度。

HLSL 最小精確度的規則類似于 C/c + +，其中運算式中的類型會決定作業的有效位數，而不是最後寫入的型別。

## <a name="testing-your-minimum-precision-shader-code"></a>測試最小精確度著色器程式碼

參考轉譯器 ([**D3D \_ 驅動程式 \_ 類型 \_ 參考**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) 可讓您大致瞭解 HLSL 著色器程式碼中的最小有效位數如何藉由量化每個 HLSL 指令至指定的精確度來運作。 這可協助您探索可能不慎依賴超過最小精確度的程式碼。 當您的 HLSL 著色器程式碼使用最小有效位數，但您可以使用它來驗證程式代碼的正確性時，參考轉譯器的執行速度會更快。  ([**D3D \_ 驅動程式 \_ 類型 \_ 變形**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)的 [變形](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp)) 不支援在 HLSL 著色器程式碼中使用最小有效位數;變形只會以完整的32位有效位數執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 