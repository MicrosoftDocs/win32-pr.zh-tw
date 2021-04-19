---
description: Windows 可攜式裝置支援下列工作屬性。
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: '工作屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995682"
---
# <a name="task-properties"></a>Task 屬性

Windows 可攜式裝置支援下列工作屬性。



| 屬性                         | VarType        | Description                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| **WPD \_ 工作 \_ 擁有者**             | **VT \_ LPWSTR** | 工作的擁有者。                                                                      |
| **WPD \_ 工作 \_ \_ 完成百分比** | **VT \_ UI4**    | 介於0和100之間的數位，指定工作的完成程度。                         |
| **WPD \_ 工作 \_ 提醒 \_ 日期**    | **VT \_ 日期**   | 值，指定何時應該傳送提醒來執行工作（如果未完成）。 |
| **WPD \_ 工作 \_ 狀態**            | **VT \_ LPWSTR** | 工作狀態的字串描述，例如「進行中」。                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




