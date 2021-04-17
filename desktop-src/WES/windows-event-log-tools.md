---
title: Windows 事件記錄檔工具
description: Windows 事件記錄檔提供下列用來建立提供者的工具。
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104374884"
---
# <a name="windows-event-log-tools"></a>Windows 事件記錄檔工具

Windows 事件記錄檔提供下列用來建立提供者的工具。



| 工具                                                           | 描述                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)  | 用來編譯檢測資訊清單和訊息文字檔的命令列公用程式。 |
| WevtUtil.exe                                                   | 一種命令列公用程式，主要是用來在電腦上註冊您的提供者。 您也可以使用它來取得提供者的中繼資料資訊、其事件，以及記錄事件的通道，以及從通道或記錄檔查詢事件。 WevtUtil.exe 工具組含在% windir% System32 中 \\ 。 如需使用資訊，請輸入 "wevtutil/？" 。<br/> 此命令僅限於系統管理員群組的成員，且必須以較高的許可權執行。|
