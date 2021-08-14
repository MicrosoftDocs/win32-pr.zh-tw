---
title: STGMEDIUM 結構
description: STGMEDIUM 結構
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da0adc98b5d774754bd2cbbccb415092d6498684a60189d6346afac82bd270a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992268"
---
# <a name="the-stgmedium-structure"></a>STGMEDIUM 結構

如同 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構是 Windows 剪貼簿格式識別碼的增強功能，因此 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構是用來傳輸資料的全域記憶體控制碼的改進。 **STGMEDIUM** 結構包括成員 **tymed**，這表示要使用的媒體，以及組成指標的等位，以及取得 **tymed** 中指定之媒體的控制碼。

[**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構可讓資料來源和取用者以每個轉譯為基礎，選擇最有效率的 exchange 媒體。 如果資料很大，而應該保留在磁片上，則資料來源可以用慣用的格式指出磁片型媒體，而只有在這是取用者瞭解的唯一媒介時，才使用全域記憶體作為備份。 能夠使用最適合交換的媒體作為預設值，可改善應用程式之間資料交換的整體效能。 例如，如果要傳送的部分資料已在磁片上，則來源應用程式可以在相同的應用程式中移動或複製到新的目的地，而不需要先將資料載入至全域記憶體。 在接收端，資料的取用者不需要將它寫回磁片。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料格式和傳輸媒體](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




