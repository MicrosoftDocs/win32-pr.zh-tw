---
description: 當您開啟物件的控制碼時，傳回的控制碼會有物件的存取權限組合。
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: 要求存取物件的存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970644"
---
# <a name="requesting-access-rights-to-an-object"></a>要求存取物件的存取權限

當您開啟物件的控制碼時，傳回的控制碼會有物件的存取權限組合。 某些功能（例如 [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)）不需要一組特定的要求存取權限。 這些函式一律會嘗試開啟控制碼來取得完整存取權。 其他功能（例如 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 和 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)）可讓您指定所需的存取權限集。 您只應要求所需的存取權限，而不是開啟完整存取的控制碼。 這可防止以非預期的方式使用控制碼，而且如果物件的 DACL 只允許有限存取，則會提高存取要求成功的機率。

使用 [一般存取權限](generic-access-rights.md) 來指定開啟物件的控制碼時所需的存取類型。 這通常比指定所有對應的標準和特定許可權來得簡單。 或者，使用允許的最大常數，要求以對 \_ 呼叫端有效的所有存取權限開啟物件。

> [!Note]  
> 最大 \_ 允許的常數不能用在 ACE 中。

 

若要取得或設定物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly)中的 SACL，請在開啟物件的控制碼時，要求 [存取 \_ 系統 \_ 安全性訪問](sacl-access-right.md) 許可權。

 

 
