---
title: TaskService. HighestVersion 屬性
description: 針對腳本，表示電腦支援的最高工作排程器版本。
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- HighestVersion 屬性工作排程器
- HighestVersion 屬性工作排程器，TaskService 物件
- TaskService 物件工作排程器、HighestVersion 屬性
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27618490fcf404936532d272402bebc03d94eb72ba8156e897f344b708d90ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959488"
---
# <a name="taskservicehighestversion-property"></a>TaskService. HighestVersion 屬性

針對腳本，表示電腦支援的最高工作排程器版本。

## <a name="syntax"></a>Syntax


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>屬性值

電腦支援之工作排程器的最高版本。 最高版本是在16位界限上分割為 MajorVersion/MinorVersion 的值。 工作排程器服務會針對主要版本傳回1，次要版本則傳回2。 您可以使用 [CLng](/previous-versions//ck4c5842(v=vs.85)) 函數來取得屬性的整數值。

## <a name="examples"></a>範例

下列程式碼會示範如何使用 [CLng](/previous-versions//ck4c5842(v=vs.85)) 函數來取得 **HighestVersion** 屬性的值。


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

