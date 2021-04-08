---
title: 關於 .NET Framework 資料類型
description: 關於 .NET Framework 資料類型
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player，.NET Framework
- Windows Media Player 物件模型，.NET Framework
- 物件模型、.NET Framework
- Windows Media Player Mobile、.NET Framework
- Windows Media Player ActiveX 控制項，.NET Framework
- Windows Media Player 的行動 ActiveX 控制項，.NET Framework
- ActiveX 控制項，.NET Framework
- .NET Framework，資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021948"
---
# <a name="about-net-framework-data-types"></a>關於 .NET Framework 資料類型

本節包含將腳本導向的物件模型參考轉譯成 Microsoft .NET Framework 基底資料類型所需的資訊。 Windows Media Player 的腳本參考幾乎擁有在 .NET Framework 型程式中使用 Windows Media Player 控制項所需的所有資訊，在大部分情況下，語法會與其他指令碼語言（例如 Microsoft JScript）的語法類似。

Windows Media Player 參考會提供 JScript 資料類型，如有必要，則會提供 c + + 轉換。 例如，方法可能會傳回 **數位** 。 JScript 會以相同方式來處理所有數位，但其他語言會區分不同類型的數位 (整數、浮點數等) 。 參考提供數位資料類型的 c + + 轉換，因為 c + + 可以使用不同的方式來處理數位。 例如，c + + 使用 **int** 資料型別作為浮點數的整數算術和 **浮** 點數。

.NET Framework 會使用稍微不同的基底資料類型系統。 下表顯示您可能使用之一般資料類型的差異。 如需有關 .NET Framework 基底資料類型以及轉換成其他資料類型系統的詳細資訊，請參閱 .NET Framework 《開發人員指南》中的系統命名空間基底資料類型的相關討論。

下表提供 .NET Framework 的類別名稱和 c # 資料型別。 其他語言的資料類型則是針對其各自語言參考中的每種語言所定義。



| 腳本資料類型 | C++ 資料型別     | .NET Framework 類別 (c # 資料類型 )  |
|------------------|-------------------|---------------------------------------|
| **Number**       | **int**           | **Int32** (**int**)                    |
| **Number**       | **long**          | **Int32** (**int**)                    |
| **Number**       | **double**        | **雙** (**雙精度**)                |
| **Number**       | **float**         | **Single** (**float**)                 |
| **String**       | **BSTR**          | **字串** (**字串**)                |
| **布林值**      | **VARIANT \_ BOOL** | **布林值** (**bool**)                 |
| **Object**       | **Object**        | **物件** (**物件**)                |



 

如果您使用 Visual Studio，可以使用 Microsoft IntelliSense 技術來判斷特定函數預期的資料類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**在 .NET Framework 方案中內嵌 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




