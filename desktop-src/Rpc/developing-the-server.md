---
title: 開發伺服器
description: 當您建立分散式應用程式的伺服器程式時，必須使用 MIDL 編譯器所產生的標頭檔和伺服器 stub。
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- 遠端程序呼叫 RPC、工作、開發伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc3405c52c48f531572ab159ad083bad93f95e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316075"
---
# <a name="developing-the-server"></a>開發伺服器

當您建立分散式應用程式的伺服器程式時，必須使用 MIDL 編譯器所產生的標頭檔和伺服器 stub。 如需詳細資訊，請參閱 [開發介面](developing-the-interface.md)。 將標頭檔包含在您的伺服器 C 程式檔中。 以撰寫您應用程式的 C 原始程式檔編譯伺服器 stub。 將產生的物件檔案與匯入程式庫連結在一起。 下圖說明此程式。

![為分散式應用程式建立伺服器程式的流程](images/srvrdev.png)

您可以從圖例的範例中看到，使用稱為 MyApp 的 MIDL 檔案來定義介面。 MIDL 編譯器使用 MyApp 來產生 MyApp. \_ c 和 myapp. h。 它也會產生用戶端存根的 C 來源檔案，但這與這項特定討論無關。 伺服器程式的 C 原始程式檔 (在此情況下，Mysrvr) 必須包含檔案 Myapp. h。 此外，它也必須包含檔案 Rpc 和 Rpcndr .h。

伺服器應用程式是以兩個檔案（Mysrvr .c 和 Rprocs）開發的。 File Mysrvr 包含讓伺服器程式啟動並執行所需的功能。 伺服器程式所提供的遠端套裝程式含在 file Rprocs 中。

Mysrvr 和 Rprocs 檔案會與 Myapp 一起編譯以產生目的檔。 \_ 然後，會將物件檔案與 RPC 執行時間程式庫和其他任何可能需要的程式庫連結在一起。 結果會是名為 Mysrvr.exe 的可執行伺服器程式。

如果您未在 Open Software Foundation 中編譯 IDL 檔案 (憑證) 相容性模式 ([**/osf**](/windows/desktop/Midl/-osf)) ，則您的伺服器程式必須提供用來配置記憶體的函式，以及用來解除配置的功能。 若為 Windows 2000 和更新版本的 Windows，建議模式為 [**/Oicf**](/windows/desktop/Midl/-oi)。 如需詳細資訊，請參閱 [如何配置和解除配置記憶體](how-memory-is-allocated-and-deallocated.md)，以及 [指標和記憶體配置](pointers-and-memory-allocation.md)。

 

 