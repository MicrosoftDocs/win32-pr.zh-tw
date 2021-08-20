---
title: 使用音訊函數處理錯誤
description: 使用音訊函數處理錯誤
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- 多媒體音訊、波形音訊錯誤
- 音訊、波形音訊錯誤
- 多媒體音訊、輔助音訊錯誤
- 音訊、輔助音訊錯誤
- 波形音訊、錯誤
- 輔助音訊，錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbb332ed0be06a829c169bdf333f3f4ce73a6e9dff81b22949174216dd4017d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141081"
---
# <a name="handling-errors-with-audio-functions"></a>使用音訊函數處理錯誤

當發生錯誤時，波形-音訊和輔助音訊函數會傳回非零值。 Windows 提供的函式會將這些錯誤值轉換成錯誤的文字描述。 應用程式仍然必須檢查錯誤值以判斷如何進行，但錯誤的文字描述可用於描述錯誤給使用者的對話方塊。

您可以使用下列函數來取出音訊錯誤值的文字描述：



| 函式                                           | 描述                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | 抓取指定之波形-音訊輸入錯誤的文字描述。  |
| [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | 抓取指定波形音訊輸出錯誤的文字描述。 |



 

唯一不會傳回錯誤值的音訊函式為 [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)、 [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)和 [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)。 如果系統中沒有任何裝置或它們遇到任何錯誤，這些函數會傳回零。

 

 