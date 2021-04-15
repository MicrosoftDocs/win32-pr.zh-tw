---
title: SystemMonitor. LogFileName 屬性
description: 抓取或設定要做為系統監視器中顯示的計數器值來源之記錄檔的名稱。
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- LogFileName 屬性 SysMon
- LogFileName 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，LogFileName 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384705"
---
# <a name="systemmonitorlogfilename-property"></a>SystemMonitor. LogFileName 屬性

抓取或設定要做為系統監視器中顯示的計數器值來源之記錄檔的名稱。

> [!Note]  
> 記錄 [**檔屬性已使此屬性過時**](systemmonitor-logfiles.md) 。

 

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property LogFileName As String
```



## <a name="property-value"></a>屬性值

記錄檔的路徑。 您可以指定絕對、相對或 UNC 路徑。 記錄檔副檔名必須是 .csv、tsv 或 .blg。

## <a name="exceptions"></a>例外狀況



| 例外狀況類型                                  | 條件                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| **System.runtime.interopservices.outattribute. COMException** | 找不到指定的檔案。 Err 值為0xC0000BD1。 |
| **System. ArgumentException**                    | 您不能指定空字串。                                    |



 

## <a name="remarks"></a>備註

這個屬性會從記錄 [**檔集合的**](systemmonitor-logfiles.md) 第一個成員傳回記錄檔名稱。

如果記錄檔集合包含一或多個 [**成員，則**](systemmonitor-logfiles.md) 設定這個屬性將會失敗。

您必須使用 Logman.exe 工具或 Perfmon MMC 嵌入式管理單元來產生您新增至此集合的記錄檔。 針對 Perfmon，計數器記錄檔位於 **效能記錄檔及警示** 下。 如需有關使用 Logman.exe 或 Perfmon 的詳細資訊，請在 **說明及支援中心** 中分別搜尋 Logman 或使用效能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





