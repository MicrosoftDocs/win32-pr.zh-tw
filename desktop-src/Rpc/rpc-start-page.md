---
title: 遠端程序呼叫
description: Microsoft Remote Procedure Call (RPC) 定義了一種強大的技術，可用於建立分散式用戶端/伺服器程式。
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- 'RPC， (查看遠端程序呼叫) '
- 遠端程序呼叫 RPC，起始頁
- 遠端程序呼叫 RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382494"
---
# <a name="remote-procedure-call"></a>遠端程序呼叫

## <a name="purpose"></a>目的

Microsoft Remote Procedure Call (RPC) 定義了一種強大的技術，可用於建立分散式用戶端/伺服器程式。 RPC 執行時間存根和程式庫會管理與網路通訊協定和通訊相關的大部分處理常式。 這可讓您將焦點放在應用程式的詳細資料，而不是網路的詳細資料。

## <a name="where-applicable"></a>適用時

RPC 可以在所有以 Windows 作業系統為基礎的用戶端/伺服器應用程式中使用。 它也可以用來建立適用于異類網路環境的用戶端和伺服器程式，這些環境包含 Unix 和 Apple 等作業系統。

## <a name="developer-audience"></a>開發人員對象

RPC 是設計來供 C/c + + 程式設計人員使用。 熟悉 Microsoft 介面定義語言 (MIDL) 和 MIDL 編譯器是必要的。

## <a name="run-time-requirements"></a>執行階段需求求

RPC 執行時間程式庫隨附于 Windows。 當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，會安裝 RPC 開發環境的元件。 如需詳細資訊，請參閱 [安裝 RPC 程式設計環境](installing-the-rpc-programming-environment.md)。

## <a name="in-this-section"></a>本節內容



| 主題                                                                           | 描述                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [最佳的 RPC 程式設計實務](best-rpc-programming-practices.md)<br/> | 有關 RPC 程式設計實務的指引，可協助建立最可能的 RPC 應用程式。<br/>                            |
| [概觀](overviews.md)<br/>                                            | 將 RPC 併入用戶端/伺服器應用程式的一般資訊。<br/>                                     |
| [參考](reference.md)<br/>                                           | RPC 類型、函數和常數的檔。<br/>                                                                 |
| [RPC NDR 引擎](rpc-ndr-engine.md)<br/>                                 | RPC 和 DCOM 元件的封送處理引擎檔，RPC 網路資料標記法 (NDR) 引擎。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft 介面定義語言 (MIDL) ](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

