---
description: 本主題提供執行播放軌之音訊串流錄製的程式。
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Track-Controlled 記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499c4cb79015effa80add4fc5369ec53f134e83f3f1b7e4cda06b09869c01386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872668"
---
# <a name="track-controlled-record"></a>Track-Controlled 記錄

本主題提供執行播放軌之音訊串流錄製的程式。

**執行播放軌控制的音訊串流錄製**

1.  選取 [檔案追蹤] 終端機至資料流程。
2.  建立檔案記錄終端機。
3.  設定檔案名。
4.  列舉 TAPI 呼叫上的資料流程。 如需這些步驟，請參閱下列程式。
5.  在檔案記錄終端機上呼叫 [**start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) 方法，以啟動串流記錄。

**列舉 TAPI 呼叫上的資料流程**

1.  建立與資料流程相同之音訊類型和方向的軌跡。
2.  設定音訊格式的追蹤屬性。 如果未設定，格式將會與資料流程格式相同。
3.  選取資料流程上的曲目。

如果在多個資料流程上選取了一個追蹤，這表示混合的資料流程。

 

 



