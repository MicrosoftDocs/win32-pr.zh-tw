---
title: 其他狀態位支援
description: 其他狀態位支援
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c281b52283796d67c476e8ee00383436bc2235a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020768"
---
# <a name="miscellaneous-status-bits-support"></a>其他狀態位支援

ActiveX 控制項容器必須辨識並支援下列 OLEMISC \_ 狀態位。



| 狀態位                           | 必要？      | 註解                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTI加值稅EWHENVISIBLE<br/>       | Yes<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTI加值稅EWHENVISIBLE<br/> | No<br/>  | 非作用中和無視窗控制項支援所需。 IGNOREACTI加值稅EWHENVISIBLE 位適用于裝載非使用中和無視窗控制項的容器。 IGNOREACTI加值稅EWHENVISIBLE 位引進為 ActiveX 控制項96規格的一部分，請參閱此檔以取得詳細資料。<br/> |
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

 

 





