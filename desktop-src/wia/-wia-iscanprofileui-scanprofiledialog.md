---
description: 顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'IScanProfileUI：： ScanProfileDialog 方法 (Scanprofileui .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: a2003471a151677b5f0fbd9ae88e9d3cf8d975525a9dbf8340c6fc1a9f2befc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965807"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>IScanProfileUI：： ScanProfileDialog 方法

顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

類型： **HWND**

擁有對話方塊的父視窗控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

對話方塊為強制回應;在對話方塊關閉之前，使用者無法切換至父視窗。

您 `<ProfileName>` `<WiaItem>` 可以在對話方塊中變更元素和元素的值。 您 `<Default>` 可以新增或刪除元素。 您無法在對話方塊中進行掃描設定檔的其他變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofileui。h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IScanProfileUI**](-wia-iscanprofileui.md)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




