---
title: 使用回呼方法
description: 使用回呼方法
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows媒體格式 SDK，回呼方法
- Windows媒體格式 SDK，以非同步方式呼叫的方法
- 回呼方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ee2bcf6587e2e9e75e18404a60c3b85fb4bac5e9f14fd0164304bcc3f3338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110058"
---
# <a name="using-the-callback-methods"></a>使用回呼方法

Windows 媒體格式 SDK 中的數個介面包含以非同步方式呼叫的方法。 這些方法大多使用回呼函式，將資訊傳遞給控制應用程式。

下列各節說明有關使用回呼方法搭配 Windows 媒體格式 SDK 的一些一般問題。



| 區段                                                                          | 描述                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [使用 OnStatus 回呼](using-the-onstatus-callback.md)                   | 描述如何執行 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法，由數個物件用來通知應用程式的 SDK 作業進度。 |
| [使用非同步呼叫的事件](using-events-with-asynchronous-calls.md) | 描述在應用程式中處理非同步方法呼叫的常見技術。                                                                                                                  |
| [使用內容參數](using-the-context-parameter.md)                   | 介紹 *pvCoNtext* 參數，其由數個回呼及其呼叫方法所共用，並說明其使用方式。                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 




