---
title: 如何實例幾何著色器
description: 幾何著色器實例允許針對每個基本類型執行相同幾何著色器的多個執行。
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 866b0cedb4de0fe2f8bf9087df6637d3a6340505289b4b773eaccd380fa4b367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067918"
---
# <a name="how-to-instance-a-geometry-shader"></a>如何：實例幾何著色器

幾何著色器實例允許針對每個基本類型執行相同幾何著色器的多個執行。 若要建立幾何著色器的實例，請將實例屬性加入至主要著色器函式，並識別著色器函式主體中的實例索引參數。

若要建立幾何著色器的實例：

1.  將 [實例屬性](sm5-attributes-instance.md) 加入至 main 函數。

    ```
    [instance(24)]
    ```

    

    這會定義每個基本 (最多可執行 32) 的實例數目。

2.  將 [ [SV \_ GSInstanceID](sv-gsinstanceid.md) 系統] 值附加至 [函數參數] 清單中的變數，可用來追蹤所執行之實例的識別碼。
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  編譯和建立著色器，就像任何其他幾何著色器一樣。

其他詳細資料包含：

-   最大實例計數為32。
-   最大頂點計數是每個實例的最大頂點計數。
-   每個實例調用 (像任何幾何著色器調用一樣) 增加調用計數，並產生隱含的 RestartStrip () 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[幾何著色器功能](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




