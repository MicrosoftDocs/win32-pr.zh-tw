---
description: 受控物件格式 (MOF) 是用來描述通用訊息模型 (CIM) 類別的語言。
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: 管理物件格式 (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ac36bd89979d6cf0de0a4d574a47a6ce7060f90e5577402eba77aa2de42bbedb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131173"
---
# <a name="managed-object-format-mof"></a>管理物件格式 (MOF)

受控物件格式 (MOF) 是用來描述 [*通用訊息模型 (CIM)*](gloss-c.md) 類別的語言。

針對 WMI 提供者執行新 WMI 類別的建議方式，是在使用 [**Mofcomp.exe**](mofcomp.md) 編譯至 [*wmi 存放庫*](gloss-w.md)的 MOF 檔案中。 您也可以使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)來建立和操作 CIM 類別和實例。

WMI 提供者通常包含 MOF 檔案，該檔案會定義提供者傳回資料的資料和事件類別，以及包含提供資料之程式碼的 DLL 檔案。 如需詳細資訊，請參閱 [將資料提供給 WMI](providing-data-to-wmi.md)。

WMI 用戶端腳本和應用程式可以查詢提供者 MOF 類別的實例，或訂閱以接收事件通知。

您可以使用 MOF 來執行下列工作：

-   [編譯 MOF 檔案](compiling-mof-files.md)
-   [建立類別](creating-a-class.md)
-   [建立實例](creating-an-instance.md)
-   [建立方法](creating-a-method.md)
-   [新增限定詞](adding-a-qualifier.md)
-   [建立批註](creating-a-comment.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 WMI](about-wmi.md)
</dt> </dl>

 

 



