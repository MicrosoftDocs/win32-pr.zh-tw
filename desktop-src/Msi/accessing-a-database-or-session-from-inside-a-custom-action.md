---
description: 您無法從非目前安裝會話的自訂動作存取安裝程式會話。
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: 從自訂動作內部存取資料庫或會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c653d14bc2fdb361469389c4ee053e5d98b65f8c8265516c4e2c3bd4fc4c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046058"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>從自訂動作內部存取資料庫或會話

您無法從非目前安裝會話的自訂動作存取安裝程式會話。 自訂動作僅限使用會話的使用中資料庫，而且沒有其他資料庫。 下列 Windows Installer[資料庫函數](database-functions.md)不能從自訂動作呼叫，因為它們需要資料庫的控制碼，而不是目前安裝會話的資料庫：

[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[從自訂動作內部存取目前的安裝程式會話](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



