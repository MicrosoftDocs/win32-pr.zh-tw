---
description: 磁片區上的每個檔案和目錄都支援個別檔案和目錄的壓縮，都有壓縮狀態。
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: 壓縮狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19abfe0deecb951c00dacb00c64dd8dcf7af56d37fe9112095cdce403619f843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582418"
---
# <a name="compression-state"></a>壓縮狀態

磁片區上的每個檔案和目錄都支援個別檔案和目錄的壓縮，都有 *壓縮狀態*。

檔案或目錄的壓縮屬性只會指出檔案或目錄是否已壓縮或未壓縮，而壓縮狀態也會指定任何壓縮資料的格式。

使用 [**FSCTL \_ 取得 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) 控制程式代碼來判斷檔案或目錄的壓縮狀態。

壓縮狀態會編碼為16位值。 壓縮格式的壓縮狀態值 \_ [ \_ 無] 表示不壓縮檔案。 壓縮 \_ 格式 \_ 預設值表示使用預設壓縮格式壓縮檔案。 任何其他值則表示壓縮檔案，使用壓縮狀態值指定的壓縮格式。

使用 [**FSCTL \_ 設定 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) 控制程式代碼來設定檔案或目錄的壓縮狀態。 此操作也會設定檔案或目錄的壓縮屬性。

將檔案的壓縮狀態設定為非零值，會使用壓縮狀態值所編碼的壓縮格式來壓縮檔案。 將檔案的壓縮狀態設定為零會解壓縮檔案。 這些是同步作業。 當您設定壓縮狀態時，就會立即壓縮或解壓縮檔案。

設定目錄的壓縮狀態不會造成任何立即壓縮或解壓縮。 相反地，設定目錄的壓縮狀態會設定預設壓縮狀態，以提供給所有新建立的檔案和子目錄。

 

 
