---
description: 印表機 DC 可以在使用點矩陣印表機、噴墨印表機、雷射印表機或繪圖器列印時使用。
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: " (Windows GDI) 的印表機裝置內容"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972565"
---
# <a name="printer-device-contexts-windows-gdi"></a> (Windows GDI) 的印表機裝置內容

印表機 DC 可以在使用點矩陣印表機、噴墨印表機、雷射印表機或繪圖器列印時使用。 應用程式會藉由呼叫 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 函式，並提供適當的引數 (印表機驅動程式的名稱、印表機的名稱、實體輸出媒體的檔案或裝置名稱，以及其他初始化資料) 來建立印表機 DC。 當應用程式完成列印時，它會藉由呼叫 [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) 函式來刪除印表機 DC。 應用程式必須刪除 (而不是) 印表機 DC 中的版本;當應用程式嘗試使用它來釋放印表機 DC 時， [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式會失敗。

如需詳細資訊，請參閱 [印表機輸出](../printdocs/printer-output.md)。

 

 
