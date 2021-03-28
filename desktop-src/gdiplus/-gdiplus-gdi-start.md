---
description: Windows GDI + 是以類別為基礎的 API，適用于 C/c + + 程式設計人員。
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112952"
---
# <a name="gdi"></a>GDI+

## <a name="purpose"></a>目的

Windows GDI + 是以類別為基礎的 API，適用于 C/c + + 程式設計人員。 它可讓應用程式在影片顯示器和印表機上使用圖形和格式化的文字。 以 Microsoft Win32 API 為基礎的應用程式不會直接存取圖形硬體。 相反地，GDI+ 會代表應用程式與裝置驅動程式進行互動。 Microsoft Win64 也支援 GDI+。

## <a name="where-applicable"></a>適用時

在 Windows 服務中不支援使用 GDI + 函式和類別。 嘗試從 Windows 服務使用這些函式和類別可能會產生未預期的問題，例如服務效能降低、執行時間例外狀況或錯誤。

> [!Note]  
> 當您使用 GDI + API 時，您絕不能讓應用程式從不受信任的來源下載任意字型。 作業系統需要較高的許可權，以確保所有已安裝的字型都受到信任。

## <a name="developer-audience"></a>開發人員對象

GDI + c + + 類別型介面是設計來供 C/c + + 程式設計人員使用。 需要熟悉 Windows 圖形使用者介面和訊息驅動架構。

## <a name="run-time-requirements"></a>執行階段需求求

GDI + 可以在所有 Windows 應用程式中使用。 GDI + 是在 Windows XP 和 Windows Server 2003 中引進。 如需有關使用特定類別或方法的作業系統需要哪些作業系統的詳細資訊，請參閱類別或方法檔集的詳細資訊一節。

## <a name="in-this-section"></a>本節內容

| 主題                                                    | 描述                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [概觀](-gdiplus-about-gdi--about.md)<br/>     | 關於 GDI + 的一般資訊。<br/>            |
| [使用](-gdiplus-using-gdi--use.md)<br/>          | 使用 GDI + 的工作和範例。<br/>             |
| [參考](-gdiplus-class-gdi-reference.md)<br/> | GDI + c + + 類別型 API 的檔。<br/> |

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows GDI](../gdi/windows-gdi.md)
</dt> <dt>

[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> <dt>

[Windows 映像取得](../wia/-wia-startpage.md)
</dt> <dt>

[Opengl](../opengl/opengl.md)
</dt> <dt>

[Windows 多媒體](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
