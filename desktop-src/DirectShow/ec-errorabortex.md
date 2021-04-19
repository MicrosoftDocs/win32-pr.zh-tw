---
description: 作業已中止，因為發生錯誤。
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: 'EC_ERRORABORTEX (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8465825b93207059e5f2ea5f054deb7c3fd5619f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983163"
---
# <a name="ec_errorabortex"></a>EC \_ ERRORABORTEX

作業已中止，因為發生錯誤。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**(HRESULT)** 失敗的作業程式碼失敗。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**(BSTR)** 包含其他錯誤資訊的字串。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

舊版 [Windows Media 來源](windows-media-source-filter.md) 篩選傳送此事件。 新的篩選器不應傳送此事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 




