---
description: 下列清單包含 CMSPStream 成員。
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: CMSPStream 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115604"
---
# <a name="cmspstream-members"></a>CMSPStream 成員



| 成員類型                     | Name                | 描述                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                        | \*m \_ pFTM           | 無限制執行緒封送處理器的指標。                                                                                                   |
| DWORD                           | m \_ dwState          | 資料流程的目前狀態。                                                                                                           |
| HANDLE                          | m \_ hAddress         | 使用此資料流程的位址。                                                                                            |
| DWORD                           | m \_ dwMediaType      | 此資料流程的 [**媒體類型**](tapimediatype--constants.md) (音訊、影片等 ) 。                                                    |
| 終端機 \_ 方向             | m \_ 方向        | 此資料流程 (傳入或傳出) 的 [**方向**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) 。                                                         |
| CMSPCallBase                    | \*m \_ pMSPCall       | 呼叫物件的指標。                                                                                                                |
| IGraphBuilder                   | \*m \_ pIGraphBuilder | 繪圖物件介面的指標。                                                                                                        |
| IMediaControl                   | \*m \_ pIMediaControl | 媒體控制項介面的指標。                                                                                                    |
| CMSPArray <ITTerminal \*> | m \_ 終端機        | 資料流程上的終端機清單。                                                                                                       |
| CMSPCritSection                 | m \_ 鎖定             | 保護資料流程物件的鎖定。 資料流程物件絕對不應該取得鎖定，然後呼叫可能會鎖定的 MSPCall 方法。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



