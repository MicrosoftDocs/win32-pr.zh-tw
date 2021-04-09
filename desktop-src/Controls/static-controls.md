---
title: 靜態控制項
description: 本章節包含與靜態控制項搭配使用之程式設計項目的相關資訊。 靜態控制項是一種控制項，可讓應用程式為使用者提供通常不需要回應的資訊文字和圖形。
ms.assetid: vs|controls|~\controls\staticcontrols\staticcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c8c5b554dad8c6f3c18d0c1ceb9300dde57b20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024178"
---
# <a name="static-control"></a>靜態控制項

本章節包含與靜態控制項搭配使用之程式設計項目的相關資訊。 *靜態控制項* 是一種控制項，可讓應用程式為使用者提供通常不需要回應的資訊文字和圖形。

### <a name="overviews"></a>概觀



| 主題                                              | 目錄                                                              |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [關於靜態控制項](about-static-controls.md) | 本主題討論如何使用靜態控制項。<br/>         |
| [靜態控制項樣式](static-control-styles.md) |                                                                       |
| [使用靜態控制項](using-static-controls.md) | 本主題提供使用靜態控制項的範例。<br/> |



 

### <a name="messages"></a>訊息



| 主題                                 | 目錄                                                                                                                                                                        |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**STM \_ GETICON**](stm-geticon.md)   | 應用程式會傳送 [**STM \_ GETICON**](stm-geticon.md) 訊息，以抓取與具有 SS 圖示樣式之靜態控制項相關聯的圖示控制碼 \_ 。 <br/> |
| [**STM \_ GETIMAGE**](stm-getimage.md) | 應用程式會傳送 [**STM \_ GETIMAGE**](stm-getimage.md) 訊息，以抓取與靜態控制項相關聯之影像的控制碼 (圖示或點陣圖) 。 <br/>          |
| [**STM \_ SETICON**](stm-seticon.md)   | 應用程式會傳送 [**STM \_ SETICON**](stm-seticon.md) 訊息，以將圖示與圖示控制項產生關聯。 <br/>                                                     |
| [**STM \_ SETIMAGE**](stm-setimage.md) | 應用程式會傳送 [**STM \_ SETIMAGE**](stm-setimage.md) 訊息，以將新的映射與靜態控制項產生關聯。<br/>                                                |



 

### <a name="notifications"></a>通知



| 主題                                           | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [STN \_ 按一下](stn-clicked.md)                 | 當使用者按一下具有 [**SS \_ 通知**](static-control-styles.md)樣式的靜態控制項時，會傳送 [STN \_ 點擊](stn-clicked.md)通知碼。 控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。<br/>                                                                                                                                                                  |
| [STN \_ DBLCLK](stn-dblclk.md)                   | 當使用者按兩下具有 **SS \_ 通知** 樣式的靜態控制項時，會傳送 [STN \_ DBLCLK](stn-dblclk.md)通知碼。 控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。<br/>                                                                                                                                                                                          |
| [STN \_ DISABLE](stn-disable.md)                 | 停用靜態控制項時，會傳送 [STN \_ 停](stn-disable.md) 用通知碼。 靜態控制項必須具有 **SS \_ 通知** 樣式才能接收此通知碼。 控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。<br/>                                                                                                                                            |
| [STN \_ 啟用](stn-enable.md)                   | 啟用靜態控制項時，會傳送 [STN \_ 啟用](stn-enable.md) 通知碼。 靜態控制項必須具有 **SS \_ 通知** 樣式才能接收此通知碼。 控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。<br/>                                                                                                                                               |
| [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) | 靜態控制項，或是唯讀或停用的編輯控制項，會在即將繪製控制項時，將 [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) 訊息傳送至其父視窗。 藉由回應此訊息，父視窗可使用指定的裝置內容控制碼來設定靜態控制項的文字和背景色彩。 <br/> 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 <br/> |



 

 

