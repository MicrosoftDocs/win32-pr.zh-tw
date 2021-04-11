---
title: 管道狀態
description: 在伺服器上，MIDL 編譯器會建立可協調 push、pull 和配置程式的狀態變數。
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092904"
---
# <a name="the-pipe-state"></a>管道狀態

在伺服器上，MIDL 編譯器會建立可協調 push、pull 和配置程式的 *狀態* 變數。 在用戶端上，開發人員必須建立 *狀態* 變數。 因此， *狀態* 變數是兩端的區域—亦即，用戶端和伺服器都維持自己的管道狀態。 伺服器 stub 程式碼會維護伺服器上的狀態變數。 您不應該嘗試直接修改它的內容。 用戶端必須初始化管道控制結構中的欄位，並維護其 *狀態* 變數。 它會使用 *狀態* 變數來識別要找出或放置資料的位置。

如果您要將資料從某個檔案傳送到另一個檔案，用戶端 *狀態* 變數可以像檔案控制代碼一樣簡單。 它也可以是指向陣列中之元素的整數。 或者，您可以定義相當複雜的狀態結構來執行其他工作，例如協調 \[ [in](/windows/desktop/Midl/in)、 [out](/windows/desktop/Midl/out-idl)參數的推送和提取常式 \] 。

 

 