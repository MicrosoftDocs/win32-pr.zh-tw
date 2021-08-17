---
title: 壓縮和解壓縮設定
description: 壓縮和解壓縮設定
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，設定壓縮機
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，設定壓縮機
- ICM_CONFIGURE 訊息
- ICQueryConfigure 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8905ea35d65fc3eda3ddee130039503d8e26555665aae9efa517cb399349475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144972"
---
# <a name="compressor-and-decompressor-configuration"></a>壓縮和解壓縮設定

您的應用程式可以自動設定壓縮程式或解壓縮程式，也可以允許使用者進行設定。 如果可行，可讓使用者設定壓縮程式或解壓縮程式;這可讓您不考慮壓縮程式或解壓縮程式的所有選項。

使用者可以使用 [設定] 對話方塊來設定 [壓縮程式] 或 [解壓縮程式]。 您可以將 [**ICM \_ 設定**](icm-configure.md)訊息傳送至 bc-vcm-lvm-hyperv (或使用 [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure)宏) 來判斷壓縮或解壓縮是否可顯示 [設定] 對話方塊。 若是如此，請傳送 ICM \_ 設定訊息 (或使用 [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure)宏) 來顯示它。

您的應用程式可以 [**傳送 \_ ICM >getstate**](icm-getstate.md)和 [**ICM \_ SETSTATE**](icm-setstate.md)訊息 (或使用 [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize)、 [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)和 [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate)宏) 來取得和設定壓縮程式或解壓縮程式的狀態。 如果您的應用程式建立或修改狀態，則必須先取得壓縮程式或解壓縮程式資料的配置，再還原其狀態。 或者，如果您的應用程式從壓縮程式或解壓縮程式取得狀態，並在後續的會話中使用它來還原狀態，則必須確保它只會還原從目前正在使用的壓縮程式或解壓縮程式取得的狀態資訊。

 

 




