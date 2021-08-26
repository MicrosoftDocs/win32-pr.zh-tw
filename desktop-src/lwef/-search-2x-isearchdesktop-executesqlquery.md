---
title: ISearchDesktop ExecuteSQLQuery 方法
description: 取得包含結構化查詢語言 (SQL)  (SQL) 查詢及其屬性的字串指標，並將指標傳回給傳回集。
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- ExecuteSQLQuery 方法舊版 Windows 環境功能
- ExecuteSQLQuery 方法舊版 Windows 環境功能，ISearchDesktop 介面
- ISearchDesktop 介面舊版 Windows 環境功能，ExecuteSQLQuery 方法
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec436a427958988e7605673b12b3fd8dc6fd3e1a54ab61cc5f542f0494c34923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014288"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>ISearchDesktop：： ExecuteSQLQuery 方法

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

取得包含結構化查詢語言 (SQL)  (SQL) 查詢及其屬性的字串指標，並將指標傳回給傳回集。

## <a name="syntax"></a>語法


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdwAttributes* \[在\]
</dt> <dd>

類型： **LPCWSTR \***

字串，包含查詢的其他屬性。

</dd> <dt>

*pwszURL* \[在\]
</dt> <dd>

類型： **LPCWSTR**

包含 SQL 查詢的字串。

</dd> <dt>

*ppidUrl* \[擴展\]
</dt> <dd>

類型： **ppidUrl \***

當這個方法成功傳回時，會包含傳回之記錄集的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

 

 




