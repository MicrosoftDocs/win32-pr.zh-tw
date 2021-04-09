---
description: 只有當要求者有一些可用提供者的相關資訊時，才應該選取特定的提供者。
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: 選取提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115140"
---
# <a name="selecting-providers"></a>選取提供者

只有當要求者有一些可用提供者的相關資訊時，才應該選取特定的提供者。

因為這通常不是這種情況，建議要求者提供 GUID \_ Null 做為 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)的提供者識別碼，讓系統根據下列演算法選擇提供者：

1.  如果有支援指定磁片區的硬體提供者可供使用，則會予以選取。
2.  如果沒有可用的硬體提供者，則如果指定的磁片區有任何特定的軟體提供者可供使用，則會予以選取。
3.  如果沒有硬體提供者和磁片區專用的軟體提供者，則會選取系統提供者。

不過，要求者可以使用 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)來取得可用提供者的相關資訊。 有了這項資訊，而且只有在備份應用程式對各種提供者有充分的瞭解時，要求者可以提供有效的提供者識別碼給 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)。

請注意，所有磁片區都不需要有相同的提供者。

 

 



