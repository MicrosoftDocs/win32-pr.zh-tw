---
title: 轉譯內容
description: OpenGL 轉譯內容是所有 OpenGL 命令通過的通訊埠。 進行 OpenGL 呼叫的每個執行緒都必須有目前的轉譯內容。 轉譯內容會將 OpenGL 連結至 Windows 的視窗化系統。
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- Windows 上的 OpenGL，轉譯內容
- 轉譯內容 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51167161662501f8aaaca6a392b2efc84217be139842c343056746abf0c35161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011946"
---
# <a name="rendering-contexts"></a>轉譯內容

OpenGL 轉譯 *內容* 是所有 OpenGL 命令通過的通訊埠。 進行 OpenGL 呼叫的每個執行緒都必須有目前的轉譯內容。 轉譯內容會將 OpenGL 連結至 Windows 的視窗化系統。

應用程式會在建立轉譯內容時，指定 Windows 的裝置內容。 此轉譯內容適用于在裝置上以指定的裝置內容參考的繪圖。 尤其是，轉譯內容與裝置內容具有相同的像素格式。 如需詳細資訊，請參閱轉譯 [內容函數](rendering-context-functions.md)。

儘管此關聯性，轉譯內容與裝置內容不同。 裝置內容包含圖形元件的相關資訊， (GDI) 的 Windows。 轉譯內容包含與 OpenGL 相關的資訊。 您必須在 GDI 呼叫中明確指定裝置內容。 轉譯內容在 OpenGL 呼叫中是隱含的。 您應該先設定裝置內容的像素格式，然後再建立轉譯內容。

進行 OpenGL 呼叫的執行緒必須有目前的轉譯內容。 如果應用程式從缺少目前呈現內容的執行緒進行 OpenGL 呼叫，就不會發生任何事;呼叫沒有任何作用。 應用程式通常會建立轉譯內容，並將它設定為執行緒的目前轉譯內容，然後呼叫 OpenGL 函數。 當它完成呼叫 OpenGL 函式時，應用程式會從執行緒 uncouples 轉譯內容，然後刪除轉譯內容。 一個視窗可以一次繪製多個轉譯內容，但一個執行緒只能有一個目前的使用中轉譯內容。

目前的轉譯內容有相關聯的裝置內容。 該裝置內容的裝置內容必須與建立轉譯內容時所使用的相同，但必須參考相同的裝置，且具有相同的像素格式。

一個執行緒只能有一個目前的轉譯內容。 轉譯內容可以只是一個執行緒的最新狀態。

 

 




