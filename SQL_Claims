
Select distinct
  AsPolicyField.TextValue As PolicyNumber
, AsPolicy.PolicyNumber As ClaimNumber
--, AsPolicyField.TextValue As PolicyNumber
, ASF2.textvalue As CauseCode
, AsSegmentField.textvalue As CauseCategory
--, ASF2.textvalue As CauseCode

From AsActivity
Join AsPolicy on AsPolicy.PolicyGUID = AsActivity.PolicyGUID
Join AsSegment on AsSegment.PolicyGUID = AsPolicy.PolicyGUID
Join AsPolicyField on AsPolicyField.PolicyGUID = AsPolicy.PolicyGUID
Join AsSegmentField on AsSegmentfield.SegmentGUID = AsSegment.SegmentGUID and AsSegmentFIeld.FieldName = 'CauseCategoryDeath'
Join AsSegmentField ASF2 on ASF2.SegmentGUID = AsSegment.SegmentGUID and ASF2.FieldName = 'CauseCodeDeath'

where AsPolicyField.TextValue in 
(
'194239401',
'340545202',
'813443211',
'994716404',
'AWN804656',
'CZE198413',
'KRP318710'
)
