---
title: 'IADsPrintJobOperations 屬性方法 (Iads .h) '
description: IADsPrintJobOperations 介面的屬性方法會讀取並寫入下表所列的屬性。 如需屬性方法的詳細資訊，請參閱介面屬性方法。
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- IADsPrintJobOperations 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f337681cb7e75a478000bd06daaac1165edaaaf1cb4255b2890347fbcff7de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691067"
---
# <a name="iadsprintjoboperations-property-methods"></a>IADsPrintJobOperations 屬性方法

[**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)介面的屬性方法會讀取並寫入下表所列的屬性。 如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**PagesPrinted**
</dt> <dd> <dl>

包含列印的頁面數目。

<dt>

存取類型：唯讀
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

**位置**
</dt> <dd> <dl>

包含列印佇列中此列印工作的位置。

<dt>

存取類型：讀取/寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

**狀態**
</dt> <dd> <dl>

包含列印工作的目前狀態，如其中一個 [**ADSI 列印工作狀態常數**](adsi-print-job-status-constants.md) 值所表示。

<dt>

存取類型：唯讀
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

**>timeelapsed**
</dt> <dd> <dl>

包含自列印工作開始以來經過的毫秒數。

<dt>

存取類型：唯讀
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>範例

下列程式碼範例會示範如何使用 [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) 的屬性。


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsPrintJobOperations 定義為32FB6780-1ED0-11CF-A988-00AA006BC149<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**ADSI 列印工作狀態常數**](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





