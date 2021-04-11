---
description: 本主題將說明如何將 XAudio2 方法群組在一起，讓它們可以同時生效。
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 使用方法：將音訊方法群組為操作集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850368"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a>使用方法：將音訊方法群組為操作集

本主題將說明如何將 XAudio2 方法群組在一起，讓它們可以同時生效。

## <a name="to-group-audio-methods-as-an-operation-set"></a>將音訊方法分組為操作集

1.  宣告全域操作集計數器。

    [Operation set](operation-sets.md)計數器可確保每個操作集都是唯一的。

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  遞增全域計數器。

    每次提交新的作業 [集](operation-sets.md)時，全域計數器應該會遞增，以確保每個集合都是唯一的。

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  藉由設定其作業 [集](operation-sets.md) 參數，將方法呼叫分組。

4.  將 [operation set](operation-sets.md) 參數設定為 global 計數器的目前值。

    在此情況下， [**IXAudio2SourceVoice：： Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) 的四個呼叫會分組為一個作業 [集](operation-sets.md)。 將通話分組會導致所有四個音效都在相同的時間內啟動。

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  開始 [操作集](operation-sets.md)。

    當您呼叫集合中的所有方法之後，請呼叫 [**IXAudio2：： CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) ，並以全域計數器的目前值來啟動 set。

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[操作集](operation-sets.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[XAudio2 操作集](xaudio2-operation-sets.md)
</dt> </dl>

 

 
