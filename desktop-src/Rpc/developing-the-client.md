---
title: 開發用戶端
description: 開發 RPC 用戶端程式與開發伺服器程式類似。 如需有關開發 RPC 伺服器程式的詳細資訊，請參閱開發伺服器。
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- 遠端程序呼叫 RPC、工作、開發用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccc719d724ecdcc5631c5f72c5190870f864e06affd45bcce3e7f2da79fb709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021891"
---
# <a name="developing-the-client"></a>開發用戶端

開發 RPC 用戶端程式與開發伺服器程式類似。 如需有關開發 RPC 伺服器程式的詳細資訊，請參閱 [開發伺服器](developing-the-server.md)。

在伺服器開發中，您的用戶端程式必須包含 MIDL 編譯器從 .idl 檔產生的標頭檔。 MIDL 編譯器也會產生包含用戶端存根的 C 來源檔案。 您必須編譯此 C 原始程式檔，並將它連結至您的用戶端程式。  (此外，MIDL 編譯器會產生包含伺服器 stub 的 C 原始程式檔，但與此討論無關。 ) 

除了使用程式檔編譯和連結用戶端 stub 之外，您還必須將匯入程式庫 (以及用戶端程式所需的任何其他程式庫) 至用戶端程式。 下圖說明建立 RPC 用戶端程式的流程。

![建立分散式應用程式之用戶端程式的流程](images/clntdev.png)

上圖中的範例將示範如何建立稱為 MyClnt.exe 的 RPC 用戶端程式。 第一個步驟是在檔案 MyApp 中定義介面。 MIDL 編譯器會使用 MyApp 來產生 \_ 包含用戶端 stub 的檔案 myapp c.。 它也會產生一個 MyApp，也就是用戶端程式必須包含的檔案 MyApp。 用戶端程式也必須包含檔案的 RPC 和 RPCNDR。

用戶端程式本身是在 MyClnt 檔案中建立的。 在實際的專案中，用戶端程式通常是由數個 C 原始程式檔所組成。 所有這些都必須一起編譯和連結。 不過，此範例只會使用一個檔案，以簡化程式。

MyClnt \_ 檔案會進行編譯並連結至 RPC 執行時間程式庫，以及用戶端程式所需的任何其他程式庫。 結果會是名為 MyClnt.exe 的可執行用戶端程式。

如果您沒有在憑證相容性模式中編譯 IDL 檔案 ([**/osf**](/windows/desktop/Midl/-osf)) ，您的用戶端程式必須提供用來配置記憶體的函式，以及用來解除配置的功能。 針對 Windows 2000 和更新版本，建議模式為 [**/Oicf**](/windows/desktop/Midl/-oi)。 如需詳細資訊，請參閱 [如何配置和解除配置記憶體](how-memory-is-allocated-and-deallocated.md)，以及 [指標和記憶體配置](pointers-and-memory-allocation.md)。

 

 