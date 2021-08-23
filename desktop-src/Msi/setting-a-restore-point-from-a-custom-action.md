---
description: 自訂動作不得呼叫 SRSetRestorePoint 函式，因為這可能會導致將還原進入點寫入 Windows Installer 安裝的中間。
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: 設定自訂動作的還原點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b30dad9f8f250c0ae82286425d092538ad8324715e632e2c5074e428454f76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628578"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>設定自訂動作的還原點

自訂動作不得呼叫 [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa)函式，因為這可能會導致將還原進入點寫入 Windows Installer 安裝的中間。

如需詳細資訊，請參閱[系統還原點和 Windows Installer](system-restore-points-and-the-windows-installer.md)。

 

 
