---
title: TaskVariables 物件
description: 腳本物件，定義可作為參數傳遞給工作處理常式的工作變數，以及工作所啟動的外部可執行檔。
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- TaskVariables 物件工作排程器
- TaskVariables 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466397"
---
# <a name="taskvariables-object"></a>TaskVariables 物件

腳本物件，定義可作為參數傳遞給工作處理常式的工作變數，以及工作所啟動的外部可執行檔。

## <a name="members"></a>成員

**TaskVariables** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**TaskVariables** 物件有這些方法。



| 方法                                         | 描述                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetCoNtext**](taskvariables-getcontext.md) | 用來在不同的步驟與相同作業實例中的工作之間共用內容。<br/> |
| [**>getinput**](taskvariables-getinput.md)     | 取得工作的輸入變數。<br/>                                                           |
| [**SetOutput**](taskvariables-setoutput.md)   | 設定工作的輸出變數。<br/>                                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





