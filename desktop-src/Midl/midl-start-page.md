---
title: Microsoft 介面定義語言
description: Microsoft 介面定義語言 (MIDL) 定義用戶端與伺服器程式之間的介面。
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- 'MIDL MIDL， (查看 Microsoft 介面定義語言 MIDL ) '
- Microsoft 介面定義語言 MIDL
- Microsoft 介面定義語言 MIDL、起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9062d5b2af18f7c3aa5ad57a4cb8f606cccc43333e4eff17d3518f72b7a064a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534968"
---
# <a name="microsoft-interface-definition-language"></a>Microsoft 介面定義語言

## <a name="purpose"></a>目的

Microsoft 介面定義語言 (MIDL) 定義用戶端與伺服器程式之間的介面。 Microsoft 在平臺軟體發展工具組中包含 MIDL 編譯器 (SDK) ，可讓開發人員建立介面定義語言 (IDL) 檔案和應用程式佈建檔 () RPC (介面和 COM/DCOM 介面進行遠端程序呼叫所需的) ACF。 MIDL 也支援產生 OLE Automation 的類型程式庫。

## <a name="where-applicable"></a>適用時

MIDL 可以在所有以 Windows 作業系統為基礎的用戶端/伺服器應用程式中使用。 它也可以用來建立適用于異類網路環境的用戶端和伺服器程式，這些環境包含 Unix 和 Apple 等作業系統。 Microsoft 支援開放式群組 (先前稱為開放式 Software Foundation) DCE 標準的 RPC 互通性。

## <a name="developer-audience"></a>開發人員對象

使用 MIDL 與 RPC 時，熟悉 C/c + + 程式設計，而且必須使用 RPC 架構。 當使用 MIDL 與 COM 時，必須熟悉 c + + 程式設計，以及將它套用至 COM 的 RPC 架構，或者也需要熟悉 OLE Automation 模型腳本和型別程式庫。

## <a name="run-time-requirements"></a>執行階段需求求

使用 MIDL 的適當執行時間程式庫包含在 Windows 中。 當您安裝 Windows SDK 時，會安裝 MIDL 編譯器和 RPC 開發環境的元件。 如需詳細資訊，請參閱 [使用 MIDL 編譯器](using-the-midl-compiler-2.md) 和 [安裝 RPC 程式設計環境](/windows/desktop/Rpc/installing-the-rpc-programming-environment)。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                               | 描述                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [概觀](about-this-guide-2.md)<br/>                                                       | MIDL 和 MIDL 編譯器的一般資訊。<br/>                   |
| [使用 MIDL 編譯器](using-the-midl-compiler-2.md)<br/>                                 | 使用 MIDL compilter 來產生 RPC 存根的相關資訊。<br/>       |
| [介面定義和型別程式庫](interface-definitions-and-type-libraries.md)<br/> | RPC 特定介面定義和類型程式庫的檔。<br/> |
| [MIDL Command-Line 參考](midl-command-line-reference.md)<br/>                           | MIDL 編譯器命令列參數的檔。<br/>               |
| [MIDL 語言參考](midl-language-reference.md)<br/>                                   | MIDL 編譯器語言參考。<br/>                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (RPC) 的遠端程序呼叫 ](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

