---
description: 在效果編譯期間會執行驗證。 若要驗證目前的技巧，請指定 Null 做為要驗證的技術控點。
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: " (Direct3D 9) 驗證"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972106"
---
# <a name="validation-direct3d-9"></a> (Direct3D 9) 驗證

在效果編譯期間會執行驗證。 若要驗證目前的技巧，請指定 **Null** 做為要驗證的技術控點。

下列任何一項的驗證將會失敗：

-   如果指定的技術控制碼不存在，則為。
-   如果任何一項技術階段中的任何狀態應用程式都失敗。
-   如果裝置驗證在應用程式的任何階段中的所有狀態都未通過之後便失敗。
-   如果無效或 VERTEXSHADER 效果狀態是在任何一次的技巧中指派了不正確著色器。
-   如果裝置 caps 不支援 cube 對應，且材質效果狀態是在任何一次的技巧中指派為 textureCUBE 類型的值。
-   如果裝置 caps 不支援磁片區對應，且材質效果狀態是在任何一次的技巧中指派為 texture3D 類型的值。

如需詳細資訊，請參閱 [效果狀態 (Direct3D 9) ](effect-states.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



