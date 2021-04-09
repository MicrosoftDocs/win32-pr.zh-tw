---
title: ACF 檔案
description: ACF 檔案可讓您自訂用戶端和/或伺服器應用程式的 RPC 介面，而不會影響介面的網路特性。
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933568"
---
# <a name="the-acf-file"></a>ACF 檔案

ACF 檔案可讓您自訂用戶端和/或伺服器應用程式的 RPC 介面，而不會影響介面的網路特性。 例如，如果您的用戶端應用程式包含只在本機電腦上具有意義的複雜資料結構，您可以在 ACF 檔案中指定該結構中的資料如何以與電腦無關的形式表示，以進行遠端程序呼叫。

本教學課程示範 ACF 檔的另一個用法—指定代表用戶端與伺服器之間連接的系結控制碼類型。 **\[** ACF 標頭中的 [**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) **\]** 屬性，可讓用戶端應用程式選取伺服器進行遠端程序呼叫。 ACF 會將 (MIDL 基本資料類型) 的控制碼定義為類型 [**控制碼 \_ t**](/windows/desktop/Midl/handle-t) 。 MIDL 編譯器會將 ACF 指定的系結控制碼名稱，hello \_ IfHandle 到它所產生的標頭檔中。 請注意，這個特定的 ACF 檔有空白主體。

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

MIDL 編譯器有一個選項 [**/app \_ config**](/windows/desktop/Midl/-app-config)，可讓您在 IDL 檔案中包含某些 ACF 屬性，例如 **隱含 \_ 控制碼**，而不是建立個別的 ACF 檔案。 如果您的應用程式不需要太多特殊設定，且嚴格憑證相容性不是問題，請考慮使用此選項。

 

 