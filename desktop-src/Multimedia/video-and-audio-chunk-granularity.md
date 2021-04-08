---
title: 影片和音訊區塊細微性
description: 影片和音訊區塊細微性
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- AVI 檔案，區塊細微性
- AVICap 類別，填充區
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932329"
---
# <a name="video-and-audio-chunk-granularity"></a>影片和音訊區塊細微性

區塊資料細微性是 AVI 檔案的邏輯區塊大小，用於寫入和取出音訊和影片資料區塊。 將音訊和影片區塊寫入磁片時，AVICap 會在必要時新增 (RIFF 「垃圾」) 區塊的填充區塊，以填滿每個資料的邏輯區塊。

您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得目前的區塊細微性設定。 目前的區塊資料細微性會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **wChunkGranularity** 成員中。 您可以指定新的區塊資料細微性作為 **wChunkGranularity** 的值，然後使用 [ [**WM \_ CAP \_ SET \_ SEQUENCE \_ 設定**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。 您也可以為此成員指定零，將區塊細微性設定為磁片的磁區大小。

 

 




