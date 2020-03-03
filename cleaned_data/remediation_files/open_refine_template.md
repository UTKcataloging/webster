# OpenRefine Template for Webster (migration)

---

## Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

## Row Template

```
<mods>
<identifier type="local">{{cells["identifier"].value}}</identifier>

<identifier type="pid">{{cells["PID"].value}}</identifier>

{{if(isBlank(cells["Archival_Number"].value),'', '<identifier type="archival number">' + cells['Archival_Number'].value + '</identifier>')}}

<titleInfo><title>{{cells["title"].value}}</title></titleInfo>

{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}

{{if(isBlank(cells['namePart'].value), '', '<name'+ if(isBlank(cells['name.URI'].value), '', ' valueURI="' + cells['name.URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['namePart'].value + '</namePart>' + if(isBlank(cells['roleTerm'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['roleTerm'].value + '</roleTerm></role>') + '</name>')}}

<originInfo>
{{if(isBlank(cells["dateCreated"].value),'','<dateCreated>' + cells['dateCreated'].value + '</dateCreated>')}}
{{if(isBlank(cells["date_edtf"].value),'','<dateCreated encoding="edtf">' + cells['date_edtf'].value + '</dateCreated>')}}
{{if(isBlank(cells["dateRange_start"].value),'','<dateCreated encoding="edtf" point="start">' + cells['dateRange_start'].value + '</dateCreated>' + '<dateCreated encoding="edtf" point="end">' + cells['dateRange_end'].value + '</dateCreated>')}}
</originInfo>

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><internetMediaType>{{cells['internetMediaType'].value}}</internetMediaType></physicalDescription>

<note displayLabel="dpn">{{cells['note'].value}}</note>


{{if(isBlank(cells['subjecttopic'].value), '', '<subject' + if(isBlank(cells['subjecttopic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subjecttopic_URI'].value + '">') + '<topic>' + cells['subjecttopic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.geographic_loc'].value), '', '<subject' + if(isBlank(cells['subject.geographic_loc_URI'].value), '>', ' authority="naf" valueURI="' + cells['subject.geographic_loc_URI'].value + '">') + '<geographic>' + cells['subject.geographic_loc'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.0topic'].value), '', '<subject' + if(isBlank(cells['subject.0topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.0topic_URI'].value + '">') + '<topic>' + cells['subject.0topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.0name'].value), '', '<subject'+ if(isBlank(cells['subject.0name_URI'].value), '', ' valueURI="' + cells['subject.0name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.0name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject.1topic'].value), '', '<subject' + if(isBlank(cells['subject.1topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.1topic_URI'].value + '">') + '<topic>' + cells['subject.1topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.1name'].value), '', '<subject'+ if(isBlank(cells['subject.1name_URI'].value), '', ' valueURI="' + cells['subject.1name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.1name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject.1geographic'].value), '', '<subject' + if(isBlank(cells['subject.1geographic_URI'].value), '>', ' authority="geonames" valueURI="' + cells['subject.1geographic_URI'].value + '">') + '<geographic>' + cells['subject.1geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.2topic'].value), '', '<subject' + if(isBlank(cells['subject.2topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.2topic_URI'].value + '">') + '<topic>' + cells['subject.2topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.2name'].value), '', '<subject'+ if(isBlank(cells['subject.2name_URI'].value), '', ' valueURI="' + cells['subject.2name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.2name'].value + '</namePart></name></subject>')}}{{if(isBlank(cells['subject.2geographic'].value), '', '<subject' + if(isBlank(cells['subject.2geographic_URI'].value), '>', ' authority="geonames" valueURI="' + cells['subject.2geographic_URI'].value + '">') + '<geographic>' + cells['subject.2geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.3topic'].value), '', '<subject' + if(isBlank(cells['subject.3topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.3topic_URI'].value + '">') + '<topic>' + cells['subject.3topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.3name'].value), '', '<subject'+ if(isBlank(cells['subject.3name_URI'].value), '', ' valueURI="' + cells['subject.3name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.3name'].value + '</namePart></name></subject>')}}{{if(isBlank(cells['subject.3geographic'].value), '', '<subject' + if(isBlank(cells['subject.3geographic_URI'].value), '>', ' authority="geonames" valueURI="' + cells['subject.3geographic_URI'].value + '">') + '<geographic>' + cells['subject.3geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.4topic'].value), '', '<subject' + if(isBlank(cells['subject.4topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.4topic_URI'].value + '">') + '<topic>' + cells['subject.4topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.4name'].value), '', '<subject'+ if(isBlank(cells['subject.4name_URI'].value), '', ' valueURI="' + cells['subject.4name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.4name'].value + '</namePart></name></subject>')}}{{if(isBlank(cells['subject.4geographic'].value), '', '<subject' + if(isBlank(cells['subject.4geographic_URI'].value), '>', ' authority="geonames" valueURI="' + cells['subject.4geographic_URI'].value + '">') + '<geographic>' + cells['subject.4geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.5topic'].value), '', '<subject' + if(isBlank(cells['subject.5topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.5topic_URI'].value + '">') + '<topic>' + cells['subject.5topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.5name'].value), '', '<subject'+ if(isBlank(cells['subject.5name_URI'].value), '', ' valueURI="' + cells['subject.5name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.5name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject.5geographic'].value), '', '<subject' + if(isBlank(cells['subject.5geographic_URI'].value), '>', ' authority="geonames" valueURI="' + cells['subject.5geographic_URI'].value + '">') + '<geographic>' + cells['subject.5geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.6topic'].value), '', '<subject' + if(isBlank(cells['subject.6topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.6topic_URI'].value + '">') + '<topic>' + cells['subject.6topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.6name'].value), '', '<subject'+ if(isBlank(cells['subject.6name_URI'].value), '', ' valueURI="' + cells['subject.6name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.6name'].value + '</namePart></name></subject>')}}{{if(isBlank(cells['subject.6geographic'].value), '', '<subject' + if(isBlank(cells['subject.6geographic_URI'].value), '>', ' authority="geonames" valueURI="' + cells['subject.6geographic_URI'].value + '">') + '<geographic>' + cells['subject.6geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.7topic'].value), '', '<subject' + if(isBlank(cells['subject.7topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.7topic_URI'].value + '">') + '<topic>' + cells['subject.7topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.7name'].value), '', '<subject'+ if(isBlank(cells['subject.7name_URI'].value), '', ' valueURI="' + cells['subject.7name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.7name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject.7geographic'].value), '', '<subject' + if(isBlank(cells['subject.7geographic_URI'].value), '>', ' authority="geonames" valueURI="' + cells['subject.7geographic_URI'].value + '">') + '<geographic>' + cells['subject.7geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.8topic'].value), '', '<subject' + if(isBlank(cells['subject.8topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.8topic_URI'].value + '">') + '<topic>' + cells['subject.8topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.8name'].value), '', '<subject'+ if(isBlank(cells['subject.8name_URI'].value), '', ' valueURI="' + cells['subject.8name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.8name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject.8geographic'].value), '', '<subject' + if(isBlank(cells['subject.8geographic_URI'].value), '>', ' authority="geonames" valueURI="' + cells['subject.8geographic_URI'].value + '">') + '<geographic>' + cells['subject.8geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.9topic'].value), '', '<subject' + if(isBlank(cells['subject.9topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.9topic_URI'].value + '">') + '<topic>' + cells['subject.9topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.9name'].value), '', '<subject'+ if(isBlank(cells['subject.9name_URI'].value), '', ' valueURI="' + cells['subject.9name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.9name'].value + '</namePart></name></subject>')}}{{if(isBlank(cells['subject.9geographic'].value), '', '<subject' + if(isBlank(cells['subject.9geographic_URI'].value), '>', ' authority="geonames" valueURI="' + cells['subject.9geographic_URI'].value + '">') + '<geographic>' + cells['subject.9geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subjectgeographic'].value), '', '<subject' + if(isBlank(cells['subjectgeographic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subjectgeographic_URI'].value + '">') + '<geographic>' + cells['subjectgeographic'].value + '</geographic></subject>')}}

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>

<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>

<relatedItem displayLabel="Collection" type="host"><titleInfo><title>{{cells['archival_collection'].value}}</title></titleInfo><identifier>{{cells['collection_identifier'].value}}</identifier></relatedItem>

<location><physicalLocation valueURI="{{cells['physicalLocation_URI'].value}}">{{cells['physicalLocation'].value}}</physicalLocation></location>

<recordInfo><recordContentSource valueURI="{{cells['source_URI'].value}}">{{cells['source'].value}}</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['Copyright_URI'].value}}">{{cells['Copyright'].value}}</accessCondition>
</mods>
```

## Row Separator

**LEAVE BLANK**

## Suffix

```
</modsCollection>
```