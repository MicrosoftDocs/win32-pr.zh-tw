---
title: 管理延遲緩衝區的變數
description: 管理延遲緩衝區的變數
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Windows Media Player 外掛程式，Echo 範例串流資源
- 外掛程式，Echo 範例串流資源
- 數位信號處理外掛程式，Echo 範例串流資源
- DSP 外掛程式，Echo 範例串流資源
- Echo DSP 外掛程式範例，串流資源
- Echo DSP 外掛程式範例，延遲緩衝區
- 延遲緩衝區
- 緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be71bc7f2ded34dcd5f29bc10ce01796b6498d36a9a194a48b0bfdec0e14662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571738"
---
# <a name="variables-to-manage-the-delay-buffer"></a>管理延遲緩衝區的變數

您必須加入管理延遲緩衝區所需的成員變數宣告。 在「私用」區段中，將下列宣告新增至 Echo：


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



將下列程式碼新增至 CEcho 的函式，以初始化延遲緩衝區變數：


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用串流資源**](working-with-streaming-resources.md)
</dt> </dl>

 

 




