---
description: 在還原作業期間，要求者可以使用 >ivssbackupcomponents：： SetRestoreState 方法來定義進行中的還原作業類型。
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: VSS 還原狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97581d33f5695890ba83e87c6f6155a9e7f92f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970178"
---
# <a name="vss-restore-state"></a>VSS 還原狀態

在還原作業期間，要求者可以使用 [**>ivssbackupcomponents：： SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) 方法來定義進行中的還原作業類型。 不過，大部分的還原作業都不需要覆寫預設的還原類型 (VSS \_ RTYPE \_ 未定義的) 。 寫入器應將此還原類型視為 \_ 由複製進行 VSS \_ RTYPE \_ 。 如需還原類型值的詳細資訊，請參閱 [**VSS \_ 還原 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) 列舉。

 

 



