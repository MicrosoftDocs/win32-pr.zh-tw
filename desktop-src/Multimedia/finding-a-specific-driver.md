---
title: 尋找特定的驅動程式
description: 尋找特定的驅動程式
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- 音訊壓縮管理員 (的) ，尋找驅動程式
- " (音效壓縮管理員) 、尋找驅動程式"
- 進行中的範例，尋找驅動程式
- 尋找驅動程式
- acmDriverEnum 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840639"
---
# <a name="finding-a-specific-driver"></a>尋找特定的驅動程式

您可能會想要讓應用程式將訊息直接傳送到特定的驅動程式，或從清單中識別特定的驅動程式。 例如，您可能想要讓應用程式識別支援篩選的驅動程式，然後查詢每個驅動程式來判斷它支援的篩選標記。 您可以使用 [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) 函數來取得所需驅動程式或驅動程式的控制碼;然後可以使用此控制碼來與該驅動程式通訊。

請注意，當應用程式安裝本機驅動程式供自己使用時， [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) 函式會傳回驅動程式控制碼，可用來與驅動程式進行通訊。 在此情況下，不需要使用 **acmDriverEnum** 。

 

 




