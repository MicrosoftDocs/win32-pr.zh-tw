---
description: 列出安全性設定附件 Dll 及其支援函數所使用的資料類型。
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: 安全性管理資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998504"
---
# <a name="security-management-data-types"></a>安全性管理資料類型

安全性管理資料類型包括下列各項：

-   [附件資料類型](#attachment-data-types)
-   [LSA 原則資料類型](#lsa-policy-data-types)

## <a name="attachment-data-types"></a>附件資料類型

安全性設定附件 Dll 和其支援的函式會使用下列資料類型。



| 資料類型                                                    | 描述                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCE \_ 列舉 \_ 內容**](sce-enumeration-context.md) | 供 [**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) 函數用來流覽安全性資料庫。                                                                                                                                              |
| [**SCE \_ 把手**](sce-handle.md)                            | 用來 [**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) 和 [**PFSCE \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) ，以便在附件和安全性資料庫之間傳遞資訊。                                                                                 |
| [**SCESTATUS**](scestatus.md)                               | 「安全性設定工具集 API」會使用資料類型來傳回函式呼叫結果的相關資訊。                                                                                                                                    |
| [**SCESVC \_ 控制碼**](scesvc-handle.md)                      | 由 [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) 和 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) 介面的方法所使用，可在 [安全性設定] 嵌入式管理單元和嵌入式管理單元擴充功能之間傳遞資訊。 |
| [**SCESVC \_ 資訊 \_ 類型**](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | 列舉是用來 [**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) 和 [**PFSCE \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) ，以指出向安全性資料庫要求或傳遞的資訊類型。                                                 |



 

## <a name="lsa-policy-data-types"></a>LSA 原則資料類型

LSA 原則管理函數會使用下列資料類型。



| 資料類型                                                  | 描述                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [**LSA \_ 列舉 \_ 控制碼**](lsa-enumeration-handle.md) | 用來追蹤需要多個函式呼叫的列舉。 |
| [**LSA \_ 控制碼**](lsa-handle.md)                          | [**原則**](policy-object.md)物件的控制碼。                       |



 

 

 
