---
title: 儲存要共用之著色器的變數和類型
description: 類別連結化物件是多個著色器可以共用之變數和類型的命名空間。
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971784"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>儲存要共用之著色器的變數和類型

類別連結化物件是多個著色器可以共用之變數和類型的命名空間。 當您在呼叫中傳遞類別連結化物件來建立著色器時，執行時間會收集可在著色器中執行每個介面的變數和類型清單，並在類別連結化物件中儲存這些變數和類型的名稱。

因此，當您呼叫 [**ID3D11ClassLinkage：： GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) 方法從類別連結化物件產生類別實例時，執行時間可以取得對應至每個著色器中所提供之名稱的變數或類型 (如果該名稱對於指定的著色器) 有效，且是以指定的類別連結化物件所建立。

例如，假設您的 **輕** 量類別會實 **色** 介面，而且您會在頂點著色器和圖元著色器中使用這個類別。 當您建立著色器 (例如，藉由呼叫 [**ID3D11Device：： CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)) ，執行時間會判斷在頂點和圖元著色器中都可使用 **light** 類別類型，並將 **燈光** 類別類型加入至類別連結化物件。 然後，您可以在想要的位置上建立 **輕** 量實例、系結這兩個著色器的資源，並在將著色器設定為裝置時，在類別實例陣列中傳遞這個實例 (例如，藉由呼叫 [**>id3d11devicecoNtext：:P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)) 。 執行時間接著會執行下列順序：

1.  確認已使用相同的類別連結化物件建立實例。
2.  確認在頂點和圖元著色器中推出 **淺色** 類別類型。
3.  選取正確的函式資料表，這在頂點和圖元著色器中可能會不同。
4.  向下傳送實例提供的位移。

類別連結化物件最終是型別和變數名稱的儲存機制。 每個專案的可用名稱數目上限 (類型和變數) 是64K。 型別和變數名稱越長，儲存體需求就越高，就是每個著色器儲存的介面中繼資料。 這是因為執行時間必須為每個著色器儲存這些名稱的對應。

## <a name="related-topics"></a>[相關主題]

[動態連結](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>相關主題

<dl> <dt>

[動態連結](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 