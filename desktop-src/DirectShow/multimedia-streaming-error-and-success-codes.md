---
description: 多媒體串流錯誤和成功碼
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: 多媒體串流錯誤和成功碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54a185b46134f4603c7adea0f1b4467da3a2cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321655"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>多媒體串流錯誤和成功碼

> [!Note]  
> 此 API 即將淘汰。 新的應用程式不應使用它。

 

下列清單包含使用多媒體串流介面的應用程式的錯誤訊息和成功通知。 這份清單不包含所有可能的錯誤;所顯示的錯誤特別適用于 Microsoft® DirectShow®多媒體串流介面的執行。



| 值                       | 十六進位碼 | Description                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MS \_ S \_ 暫止              | 0x00040001       | 範例更新尚未完成。                                                                                                                                                         |
| MS \_ S \_ NOUPDATE             | 0x00040002       | 未在強制完成後更新範例。                                                                                                                                            |
| MS \_ S \_ ENDOFSTREAM          | 0x00040003       | 資料流程的結尾。 範例未更新。                                                                                                                                                         |
| MS \_ E \_ SAMPLEALLOC          | 0x80040401       | 無法從 [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)物件移除 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)物件，因為它仍包含至少一個已配置的範例。 |
| MS \_ E \_ PURPOSEID            | 0x80040402       | 指定的目的識別碼無法用於呼叫。                                                                                                                                       |
| MS \_ E \_ NOSTREAM             | 0x80040403       | 找不到具有指定屬性的資料流程。                                                                                                                                      |
| MS \_ E \_ NOSEEKING            | 0x80040404       | 這個 [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) 物件不支援搜尋。                                                                                                      |
| MS \_ E \_ 不相容         | 0x80040405       | 資料流程格式不相容。                                                                                                                                                     |
| MS \_ E \_ 忙碌                 | 0x80040406       | 此範例忙碌中。                                                                                                                                                                        |
| MS \_ E \_ NOTINIT              | 0x80040407       | 物件無法接受呼叫，因為未呼叫其 initialize 函數或對等專案。                                                                                        |
| MS \_ E \_ SOURCEALREADYDEFINED | 0x80040408       | 來源已定義。                                                                                                                                                                    |
| MS \_ E \_ INVALIDSTREAMTYPE    | 0x80040409       | 資料流程類型對這項作業無效。                                                                                                                                           |
| MS \_ E \_ NOTRUNNING           | 0x8004040A       | [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)物件未處於執行中狀態。                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多媒體串流](multimedia-streaming.md)
</dt> </dl>

 

 



