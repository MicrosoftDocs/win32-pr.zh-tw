---
title: 索引大小
description: 索引大小
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673923"
---
# <a name="index-size"></a>索引大小

每個 AVI 檔案都會使用指定大小的索引，以找出檔案內的影片和音訊資料區塊。 索引中的專案會尋找一個影片框架或波形音訊緩衝區。 因此，索引大小的值會間接設定可在檔案中捕捉的畫面格數目上限。

您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得目前的索引大小。 目前的索引大小會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **dwIndexSize** 成員中。 您可以指定新的索引大小作為 **dwIndexSize** 的值，然後使用 [ [**WM \_ CAP \_ SET \_ SEQUENCE \_ 設定**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。 預設的索引大小為34952個專案 (允許32K 框架和) 的音訊緩衝區數目。

 

 




