---
description: 由於 Microsoft Windows XP 的非平板電腦版本缺少辨識器，因此您無法使用 InkEdit 在 Windows 2000、Windows Server 2003 和非 tablet pc 版本的 Windows XP 上轉譯筆墨，也無法使用此控制項在這些作業系統上輸入筆墨。
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: 在舊版 Windows 上使用 InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa98089a2ede778be09719767f96a1129a1be0d4004828172651e637cd81d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966607"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>在舊版 Windows 上使用 InkEdit

由於 Microsoft Windows XP 的非平板電腦版本缺少辨識器，因此您無法使用[InkEdit](inkedit-control.md)在 Windows 2000、Windows Server 2003 和非 tablet pc 版本的 Windows XP 上轉譯筆墨，也無法使用此控制項在這些作業系統上輸入筆墨。

控制項的 [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) 屬性設定為 **停用** (針對 c + +) **\_ 停用的 IEM** ，而且嘗試變更屬性沒有任何作用。 您可以將值指派給其他屬性，並將筆墨複製和貼上至其他應用程式，但您無法使用控制項來接受手勢或收集筆跡。

 

 



