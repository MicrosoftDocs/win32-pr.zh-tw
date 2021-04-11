---
description: 應用程式內容可以用來建立並存的 Windows 類別。
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: 建立並存的 Windows 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849907"
---
# <a name="creating-side-by-side-windows-classes"></a>建立並存的 Windows 類別

應用程式內容可以用來建立並存的 Windows 類別。 藉由使用並存的 Windows 類別，您的應用程式可以在獨立的父視窗中同時有不同版本的可用類別。 若要建立並存的 Windows 類別，您的應用程式必須先啟用啟用內容，然後再呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 來取得新視窗的控制碼。

例如，Windows 通用控制項5.82 版和6.0 版都有編輯控制項。 Windows 預設為使用5.82 版編輯控制項。 若要取得具有版本6.0 編輯控制項的並列視窗，在正常呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 之前，您的應用程式可以參考公開命名視窗類別的元件，然後啟動參考6.0 版控制項的啟用內容。

 

 
