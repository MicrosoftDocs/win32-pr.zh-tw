---
description: WIA 將攝影機裝置表示為 IWiaItem 物件的階層式樹狀結構。
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: WIA 攝影機裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191387"
---
# <a name="wia-camera-devices"></a>WIA 攝影機裝置

WIA 將攝影機裝置表示為 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件的階層式樹狀結構。 從 Windows 映像取得的呼叫所傳回的根專案 (WIA) 裝置管理員 [**IWiaDevMgr：： CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) 方法，可用來取得及設定裝置資訊、控制裝置，以及開始裝置專案列舉。

> [!Note]  
> WIA 不支援 Windows Vista 或更新版本中的相機。 針對這些版本的 Windows，請使用 Windows 驅動程式開發工具組中所述的 Windows 可攜式裝置 (WPD) API (DDK) 從相機取得映射。

 

下圖說明攝影機執行範例。 攝影機根專案有三個子專案，兩張圖片和一個資料夾。 資料夾有兩個子專案，這兩張圖片。

![範例攝影機執行](images/wihierar.gif)

 

 



