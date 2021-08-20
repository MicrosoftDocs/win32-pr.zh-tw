---
title: 使用視窗訊息來管理 Waveform-Audio 記錄
description: 使用視窗訊息來管理 Waveform-Audio 記錄
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- 波形音訊，使用訊息管理錄製
- 波形-音訊介面，使用訊息管理錄製
- 錄製波形音訊，使用訊息管理錄製
- 波形音訊，訊息
- 波形-音訊介面，訊息
- 錄製波形音訊，訊息
- MM_WIM_CLOSE 訊息
- MM_WIM_DATA 訊息
- MM_WIM_OPEN 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c709df27be25a8a3f4c5a9be6528e28b4e8bab9251b04b6c397a7ef3fc8efd9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135650"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a>使用視窗訊息來管理 Waveform-Audio 記錄

您可以將下列訊息傳送至視窗程式函式，以管理波形音訊錄製。



| 訊息                                | 描述                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WIM \_ 關閉**](mm-wim-close.md) | 在使用 [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) 函式關閉裝置時傳送。                                     |
| [**MM \_ WIM \_ 資料**](mm-wim-data.md)   | 當設備磁碟機使用 [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) 函式傳送的緩衝區完成時傳送。 |
| [**MM \_ WIM \_ 開啟**](mm-wim-open.md)   | 在使用 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) 函式開啟裝置時傳送。                                       |



 

[**MM \_ WIM \_ 資料**](mm-wim-data.md)的 *lParam* 參數會指定識別緩衝區之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的指標。 此緩衝區可能不會完全以波形-音訊資料填滿;記錄可能會在緩衝區填滿之前停止。 您可以使用 **WAVEHDR** 結構的 **dwBytesRecorded** 成員，判斷存在於緩衝區中的有效資料量。

最有用的訊息可能是 [**以 \_ WIM \_ 資料為 MM**](mm-wim-data.md)。 當您的應用程式使用設備磁碟機所傳送的資料區塊完成時，您可以清除並釋放資料區塊。 除非您需要配置記憶體或初始化變數，否則您可能不需要使用 [**mm \_ wim \_ 開啟**](mm-wim-open.md) 和 [**mm \_ wim \_ 關閉**](mm-wim-close.md) 訊息。

波形音訊輸入裝置的回呼函式是由應用程式所提供。 如需此回呼函數的詳細資訊，請參閱 [**waveInProc**](/previous-versions//dd743849(v=vs.85)) 函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製波形音訊](recording-waveform-audio.md)
</dt> </dl>

 

 