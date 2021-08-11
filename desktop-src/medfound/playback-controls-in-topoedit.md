---
description: TopoEdit 中的播放控制項
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: TopoEdit 中的播放控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c59dfceb30f839ba58d37385a3178d42429eb858c98f3f5196dd95141ac2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239674"
---
# <a name="playback-controls-in-topoedit"></a>TopoEdit 中的播放控制項

拓撲解決之後，它會排入媒體會話以供播放。 TopoEdit 提供在媒體會話上變更拓撲狀態的傳輸控制。

下表顯示功能表/工具列命令和每個作業的對等媒體基礎方法。



| 功能表/工具列命令                                                                                                                                                                                                                          | 媒體基礎方法                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 在 [**控制項**] 功能表上，按一下 [**播放**]。 \[換行 \] 或換行的方式， \[ \] 請按一下工具列上的 [**播放**] 按鈕 (下圖) 所示。 \[[播放] 按鈕的換行 \] ![ 螢幕擷取畫面](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| 在 [**控制項**] 功能表上，按一下 [**停止**]。 \[換行 \] 或換行的方式， \[ \] 請按一下工具列上的 [**停止**] 按鈕 (如下圖所示) 。 \[\] ![ [停止] 按鈕的換行螢幕擷取畫面](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**IMFMediaSession：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| 在 [**控制項**] 功能表上，按一下 [**暫停**]。 \[換行 \] 或換行的方式， \[ \] 請按一下工具列上的 [**暫停**] 按鈕 (如下圖所示) 。 \[\] ![ [暫停] 按鈕的換行螢幕擷取畫面](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

如需使用媒體基礎 Api 以程式設計方式控制播放的相關資訊，請參閱 [如何控制呈現狀態](how-to-control-presentation-states.md)。

## <a name="seeking"></a>尋求

如果拓撲是可搜尋的，您可以使用下圖所示的搜尋列 (進行搜尋，) 指定拓撲的時間軸中的位置開始播放。

![搜尋列的螢幕擷取畫面](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> 如果媒體來源是可搜尋的，則 [停止] 命令也會將拓撲搜尋回資料流程的開頭。

 

## <a name="changing-the-playback-rate"></a>變更播放速率

如果拓撲的基礎媒體來源支援多種播放率，您可以使用費率列來變更播放速率。 若要在媒體會話上向前快轉拓撲，請將滑杆向右拖曳，以增加速率，如下圖所示。

![費率列的螢幕擷取畫面](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> 在此版本中，TopoEdit 僅支援正數費率。 不支援反向播放。

 

如需使用媒體基礎 Api 以程式設計方式變更播放速率的詳細資訊，請參閱 [關於速率控制](about-rate-control.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TopoEdit 功能表](topoedit-menus.md)
</dt> <dt>

[TopoEdit 工具列](topoedit-toolbar.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



