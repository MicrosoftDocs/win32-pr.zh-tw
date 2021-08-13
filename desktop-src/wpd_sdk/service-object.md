---
description: 服務物件
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: 服務物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587ca25e1e9fc225a0b555263bf3f3f4e725c83e5f9b01e716fd6fa191fc270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445580"
---
# <a name="service-object"></a>服務物件

服務物件必須支援下列屬性。



| 屬性名稱                                                                                                                      | 必要或選擇性                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                         | 必要。 .                                                                           |
| [WPD \_ 物件 \_ 父 \_ 識別碼](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                   | 必要。                                                                             |
| [WPD \_ 物件 \_ 名稱](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                   | 必要。                                                                             |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85)) | 必要。                                                                             |
| [WPD \_ 物件 \_ ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | 如果不應該對使用者顯示服務物件，則為必要。                       |
| [WPD \_ 物件 \_ ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | 如果物件為系統物件，則為必要項 (例如，它代表) 的系統檔案。 |
| [WPD \_ 功能 \_ 物件 \_ 類別](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))     | 必要。 這代表裝置服務類型，例如服務連絡人。          |
| [WPD \_ 服務 \_ 版本](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                       | 必要。                                                                             |
| [WPD \_ 儲存體 \_ 類型](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))                                                | 如果服務用來儲存物件，則為必要項。                                     |
| [WPD \_ 儲存體 \_ 容量](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))                                    | 如果服務用來儲存物件，則為必要項。                                     |



 

## <a name="typical-resources"></a>一般資源

這些物件通常不會裝載資源。

## <a name="typical-formats"></a>一般格式

下列清單會識別服務物件所使用的一般格式。 不過，此物件不限於這些格式。

-   \_ \_ 未指定 WPD 物件格式 \_

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 
