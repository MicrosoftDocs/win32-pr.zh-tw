---
title: 其他狀態位支援
description: 其他狀態位支援
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d491e4f9ab3e41cf42510beeeb037e3b58e80a5f02ebe8e86e8bb07f3be5cb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096918"
---
# <a name="miscellaneous-status-bits-support"></a>其他狀態位支援

ActiveX控制容器必須辨識並支援下列 OLEMISC \_ 狀態位。



| 狀態位                           | 必要？      | 註解                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTI加值稅EWHENVISIBLE<br/>       | Yes<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTI加值稅EWHENVISIBLE<br/> | No<br/>  | 非作用中和無視窗控制項支援所需。 IGNOREACTI加值稅EWHENVISIBLE 位適用于裝載非使用中和無視窗控制項的容器。 IGNOREACTI加值稅EWHENVISIBLE 位是 ActiveX Controls 96 規格的一部分引進，請參閱這份檔以取得詳細資料。<br/> |
| INSIDEOUT<br/>                 | No<br/>  | 通常不會與 ActiveX 控制項搭配使用，而是使用複合檔案內嵌。 請注意，這與某些 SDK 檔相反，此位必須設定為要設定 ACTI加值稅EWHENVISIBLE 位。<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Yes<br/> | 指定應在設計階段顯示的控制項，但在執行時間不可見。<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Yes<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | No<br/>  | 雖然檔樣式的容器不需要支援，但通常是強制性的支援。<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | No<br/>  | 雖然檔樣式的容器不需要支援，但通常是強制性的支援。<br/>                                                                                                                                                                                                    |
| NOUIACTI加值稅E<br/>              | Yes<br/> |                                                                                                                                                                                                                                                                                                         |
| ALIGNABLE<br/>                 | No<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | No<br/>  | 查看[簡單的框架網站](simple-frame-site-containment.md)內含專案<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | No<br/>  | 建議使用此位的支援，但不是強制性。<br/>                                                                                                                                                                                                                                       |
| IMEMODE<br/>                   | No<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

 





