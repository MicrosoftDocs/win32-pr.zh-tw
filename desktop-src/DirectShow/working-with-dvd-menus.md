---
description: 使用 DVD 功能表
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: 使用 DVD 功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982120"
---
# <a name="working-with-dvd-menus"></a>使用 DVD 功能表

當使用者啟用按鈕時，或當導覽器進入第一個 Play 網域時，DVD 導覽器可能會顯示功能表。 若要以程式設計方式顯示功能表，請呼叫 [**IDvdControl2：： ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) 方法。

有幾種方式可以透過程式設計方式選取功能表按鈕：

-   若要依數位選取按鈕，請呼叫 [**IDvdControl2：： SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)。 按鈕的編號為1到36。 [**IDvdInfo2：： GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton)方法會傳回可用的按鈕數目。
-   若要選取相對於目前所選按鈕位置的按鈕，請呼叫 [**IDvdControl2：： SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton)。 您可以選取 [上]、[下]、[左] 或 [右] 方向的按鈕。
-   若要依視窗內的座標選取按鈕，請呼叫 [**IDvdControl2：： SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition)。 這個方法會採用相對於影片視窗工作區的 (x，y) 座標。  (無視窗模式，這是應用程式視窗。 ) 如果該位置沒有任何按鈕，此方法會傳回 VFW \_ E \_ DVD \_ no \_ 按鈕。

此外，還有數種方式可以啟用按鈕：

-   若要依數位啟動按鈕，請呼叫 [**IDvdControl2：： SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)。
-   若要依據按鈕的座標啟動按鈕，請呼叫 [**IDvdControl2：： ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition)。
-   若要啟動目前選取的按鈕，請呼叫 [**IDvdControl2：： ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)。 如果未選取任何按鈕，此方法會傳回 VFW \_ E \_ DVD \_ no \_ 按鈕。

請記住，選取按鈕只會反白顯示其框線。 若要引發相關聯的命令，必須啟用按鈕。 以程式設計方式啟用按鈕可透過各種方式來完成，但您必須一律先選取按鈕，才能啟用它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



